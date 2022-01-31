---
UID: NE:shobjidl_core.STPFLAG
title: STPFLAG (shobjidl_core.h)
description: Used by the ITaskbarList4::SetTabProperties method to specify tab properties.
helpviewer_keywords: ["STPFLAG","STPFLAG enumeration [Windows Shell]","STPF_NONE","STPF_USEAPPPEEKALWAYS","STPF_USEAPPPEEKWHENACTIVE","STPF_USEAPPTHUMBNAILALWAYS","STPF_USEAPPTHUMBNAILWHENACTIVE","_shell_STPFLAG","shell.STPFLAG","shobjidl_core/STPFLAG","shobjidl_core/STPF_NONE","shobjidl_core/STPF_USEAPPPEEKALWAYS","shobjidl_core/STPF_USEAPPPEEKWHENACTIVE","shobjidl_core/STPF_USEAPPTHUMBNAILALWAYS","shobjidl_core/STPF_USEAPPTHUMBNAILWHENACTIVE"]
old-location: shell\STPFLAG.htm
tech.root: shell
ms.assetid: 7d50e4fe-1689-4dbd-b367-f4881d8d5d78
ms.date: 12/05/2018
ms.keywords: STPFLAG, STPFLAG enumeration [Windows Shell], STPF_NONE, STPF_USEAPPPEEKALWAYS, STPF_USEAPPPEEKWHENACTIVE, STPF_USEAPPTHUMBNAILALWAYS, STPF_USEAPPTHUMBNAILWHENACTIVE, _shell_STPFLAG, shell.STPFLAG, shobjidl_core/STPFLAG, shobjidl_core/STPF_NONE, shobjidl_core/STPF_USEAPPPEEKALWAYS, shobjidl_core/STPF_USEAPPPEEKWHENACTIVE, shobjidl_core/STPF_USEAPPTHUMBNAILALWAYS, shobjidl_core/STPF_USEAPPTHUMBNAILWHENACTIVE
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: STPFLAG
req.redist: 
ms.custom: 19H1
f1_keywords:
 - STPFLAG
 - shobjidl_core/STPFLAG
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - shobjidl_core.h
api_name:
 - STPFLAG
---

# STPFLAG enumeration


## -description

Used by the <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist4-settabproperties">ITaskbarList4::SetTabProperties</a> method to specify tab properties.

## -enum-fields

### -field STPF_NONE:0

No specific property values are specified. The default behavior is used: the tab window provides a thumbnail and peek image, either live or static as appropriate.

### -field STPF_USEAPPTHUMBNAILALWAYS:0x1

Always use the thumbnail provided by the main application frame window rather than a thumbnail provided by the individual tab window. Do not combine this value with STPF_USEAPPTHUMBNAILWHENACTIVE; doing so will result in an error.

### -field STPF_USEAPPTHUMBNAILWHENACTIVE:0x2

When the application tab is active and a live representation of its window is available, use the main application's frame window thumbnail. At other times, use the tab window thumbnail. Do not combine this value with STPF_USEAPPTHUMBNAILALWAYS; doing so will result in an error.

### -field STPF_USEAPPPEEKALWAYS:0x4

Always use the peek image provided by the main application frame window rather than a peek image provided by the individual tab window. Do not combine this value with STPF_USEAPPPEEKWHENACTIVE; doing so will result in an error.

### -field STPF_USEAPPPEEKWHENACTIVE:0x8

When the application tab is active and a live representation of its window is available, show the main application frame in the peek feature. At other times, use the tab window. Do not combine this value with STPF_USEAPPPEEKALWAYS; doing so will result in an error.
