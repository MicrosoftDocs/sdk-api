---
UID: NE:shobjidl_core.STPFLAG
title: STPFLAG
author: windows-sdk-content
description: Used by the ITaskbarList4::SetTabProperties method to specify tab properties.
old-location: shell\STPFLAG.htm
old-project: shell
ms.assetid: 7d50e4fe-1689-4dbd-b367-f4881d8d5d78
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: STPFLAG, STPFLAG enumeration [Windows Shell], STPF_NONE, STPF_USEAPPPEEKALWAYS, STPF_USEAPPPEEKWHENACTIVE, STPF_USEAPPTHUMBNAILALWAYS, STPF_USEAPPTHUMBNAILWHENACTIVE, _shell_STPFLAG, shell.STPFLAG, shobjidl_core/STPFLAG, shobjidl_core/STPF_NONE, shobjidl_core/STPF_USEAPPPEEKALWAYS, shobjidl_core/STPF_USEAPPPEEKWHENACTIVE, shobjidl_core/STPF_USEAPPTHUMBNAILALWAYS, shobjidl_core/STPF_USEAPPTHUMBNAILWHENACTIVE
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
tech.root: 
req.typenames: STPFLAG
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - shobjidl_core.h
api_name:
 - STPFLAG
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 6.01
---

# STPFLAG enumeration


## -description


Used by the <a href="https://msdn.microsoft.com/cc3fec4b-7770-44af-9892-239a17dd96b8">ITaskbarList4::SetTabProperties</a> method to specify tab properties.


## -enum-fields




### -field STPF_NONE

No specific property values are specified. The default behavior is used: the tab window provides a thumbnail and peek image, either live or static as appropriate.


### -field STPF_USEAPPTHUMBNAILALWAYS

Always use the thumbnail provided by the main application frame window rather than a thumbnail provided by the individual tab window. Do not combine this value with STPF_USEAPPTHUMBNAILWHENACTIVE; doing so will result in an error.


### -field STPF_USEAPPTHUMBNAILWHENACTIVE

When the application tab is active and a live representation of its window is available, use the main application's frame window thumbnail. At other times, use the tab window thumbnail. Do not combine this value with STPF_USEAPPTHUMBNAILALWAYS; doing so will result in an error.


### -field STPF_USEAPPPEEKALWAYS

Always use the peek image provided by the main application frame window rather than a peek image provided by the individual tab window. Do not combine this value with STPF_USEAPPPEEKWHENACTIVE; doing so will result in an error.


### -field STPF_USEAPPPEEKWHENACTIVE

When the application tab is active and a live representation of its window is available, show the main application frame in the peek feature. At other times, use the tab window. Do not combine this value with STPF_USEAPPPEEKALWAYS; doing so will result in an error.

