# TarForge — Design Philosophy

TarForge is a deterministic packaging tool responsible for producing reproducible tarball artifacts from user-supplied filesystem trees.  
The design principles are:

1. **Determinism**  
   Given identical input directories and configuration, TarForge must produce byte-identical output tarballs.

2. **Minimalism**  
   TarForge performs one task: packaging. It does not create filesystems, download OS images, or interpret distribution semantics. Rootfs creation is the responsibility of the user or other components in the Screaming Penguin toolchain.

3. **Composability**  
   TarForge integrates with Screaming Penguin’s installer, CI pipelines, and user workflows. Artifacts must be well-structured and machine-verifiable.

4. **Transparency**  
   TarForge writes clear manifests, explicit metadata, and human-readable logs.

5. **Predictable Failure**  
   Errors must be explicit, actionable, and never destructive. TarForge must not modify input trees.

6. **No OS Redistribution**  
   All operating system content is user-provided. TarForge does not fetch or distribute OS images of any kind.

These principles guide all future phases and code decisions.
