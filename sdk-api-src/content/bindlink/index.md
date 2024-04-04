---
UID: NA:bindlink
tech.root: fs
title: bindlink (bindlink.h)
ms.date: 04/24/2023
targetos: Windows
description: This API allows admin users to bind a filesystem namespace to a local virtual path via the Bind Filter.
prerelease: false
req.assembly: 
req.construct-type: apiset
req.ddi-compliance: 
req.dll: bindlink.dll
req.header: bindlink.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: bindlink.lib
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.target-type: 
req.typenames: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - bindlink.h
api_name:
 - bindlink
f1_keywords:
 - bindlink
 - bindlink/bindlink
dev_langs:
 - c++
helpviewer_keywords:
 - bindlink
---

## -description

This API allows admin users to bind a filesystem namespace to a local "virtual path" via the Bind Filter (mini filter bindflt.sys). Bind Links provide file system redirection from a local "virtual path" to a local or remote "backing path". They can primarily enable two kinds of scenarios: first, they can make remote files over a network share appear local which improves app compatibility, and second, they enable scenarios where an application wants files from different locations to  appear in a new location, potentially with different names and directory structures, without copying the files. Bind Links are transparent to applications and all existing APIs work without the knowledge of this redirection. No physical file or directory is created for the virtual path and bind links extend the security descriptors and permissions of the files and directories in the backing path to the virtual path.

## -remarks

Bind Links are different from filesystem hard links in that they can apply across volumes while hard links can only be applied within one volume. Hard links are also limited to files, whereas bind links can map directories as well. They are also different from symbolic links in how they report their name: when a symbolic link is opened and its name is queried, the target name is returned, however, when a bind link is opened and its name is queried, the virtual name is returned. While hard links and symbolic links are persistent, bind links are ephemeral in nature. They exist until the system is shutdown. In addition to these key differences, bind links support various other functionalities, as explained below, that neither symbolic links, nor hard links support (like exceptions, read only links and merged links).

## -see-also
