---
UID: NF:shlobj_core.SHILCreateFromPath
title: SHILCreateFromPath function
author: windows-driver-content
description: SHILCreateFromPath may be altered or unavailable.
old-location: shell\SHILCreateFromPath.htm
old-project: shell
ms.assetid: 08700af7-9dbd-4162-8578-bfa47e3db6bf
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: SHILCreateFromPath, SHILCreateFromPath function [Windows Shell], _win32_SHILCreateFromPath, shell.SHILCreateFromPath, shlobj_core/SHILCreateFromPath
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: shlobj_core.h
req.include-header: Shlobj.h
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
req.typenames: AUTOCOMPLETELISTOPTIONS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Shell32.dll
-	ext-ms-win-shell-shell32-l1-2-1.dll
-	Ext-MS-Win-Shell-Shell32-L1-2-2.dll
api_name:
-	SHILCreateFromPath
product: Windows
targetos: Windows
req.lib: Shell32.lib
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
req.product: Internet Explorer 5.0
---

# SHILCreateFromPath function


## -description


<p class="CCE_Message">[<b>SHILCreateFromPath</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Applications should use <a href="https://msdn.microsoft.com/7bdfeed5-dcd0-40f6-a9d0-08ce816ee055">SHParseDisplayName</a> instead]

Creates a pointer to an item identifier list (PIDL) from a path.


## -parameters




### -param pszPath [in]

Type: <b>PCWSTR</b>

A pointer to a null-terminated string of maximum length MAX_PATH containing the path to be converted.


### -param ppidl [out]

Type: <b>PIDLIST_ABSOLUTE*</b>

The path in <i>pszPath</i> expressed as a PIDL.


### -param rgfInOut

TBD




#### - rgflnOut [in, out, optional]

Type: <b>DWORD*</b>

A pointer to a <b>DWORD</b> value that, on entry, indicates any attributes of the folder named in <i>pszPath</i> that the calling application would like to retrieve along with the PIDL. On exit, this value contains those requested attributes. For a list of possible attribute flags for this parameter, see <a href="https://msdn.microsoft.com/3864b386-7653-4661-880c-e96c08ff0dbb">IShellFolder::GetAttributesOf</a>.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



