---
UID: NS:shlobj_core._CSFV
title: "_CSFV"
author: windows-sdk-content
description: Used with the SHCreateShellFolderViewEx function.
old-location: shell\CSFV.htm
old-project: shell
ms.assetid: 9ec22fd4-1562-4ef0-b932-ebbf06082807
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: "*LPCSFV, CSFV, CSFV structure [Windows Shell], LPCSFV, LPCSFV structure pointer [Windows Shell], _CSFV, _win32_CSFV, shell.CSFV, shlobj_core/CSFV, shlobj_core/LPCSFV"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: shlobj_core.h
req.include-header: Shlobj.h
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: CSFV, *LPCSFV
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - shlobj_core.h
api_name:
 - CSFV
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 5.0
---

# _CSFV structure


## -description


Used with the <a href="https://msdn.microsoft.com/7edd6786-7d74-4065-8cf1-cbb489007a46">SHCreateShellFolderViewEx</a> function.


## -struct-fields




### -field cbSize

Type: <b>UINT</b>

The size of the <b>CSFV</b> structure, in bytes.


### -field pshf

Type: <b><a href="https://msdn.microsoft.com/35190a72-298b-4554-b924-e1357b583a99">IShellFolder</a>*</b>

A pointer to the <a href="https://msdn.microsoft.com/35190a72-298b-4554-b924-e1357b583a99">IShellFolder</a> object for which to create the view.


### -field psvOuter

Type: <b><a href="https://msdn.microsoft.com/91438583-e4f1-456f-a130-2a45846fd725">IShellView</a>*</b>

A pointer to the parent <a href="https://msdn.microsoft.com/91438583-e4f1-456f-a130-2a45846fd725">IShellView</a> interface. This parameter can be <b>NULL</b>.


### -field pidl

Type: <b>PCIDLIST_ABSOLUTE</b>

Ignored.


### -field lEvents

Type: <b>LONG</b>


### -field pfnCallback

Type: <b><a href="https://msdn.microsoft.com/744c2b49-017e-4284-a39b-3d317e483316">LPFNVIEWCALLBACK</a></b>

A pointer to the <a href="https://msdn.microsoft.com/744c2b49-017e-4284-a39b-3d317e483316">LPFNVIEWCALLBACK</a> function used by this folder view to handle callback messages. This parameter can be <b>NULL</b>.


### -field fvm

Type: <b><a href="https://msdn.microsoft.com/16b92115-6e7d-41d3-960d-6783d779224c">FOLDERVIEWMODE</a></b>

