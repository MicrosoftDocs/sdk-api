---
UID: NF:shlobj_core.SHCreateStdEnumFmtEtc
title: SHCreateStdEnumFmtEtc function
author: windows-sdk-content
description: SHCreateStdEnumFmtEtc may be altered or unavailable.
old-location: shell\SHCreateStdEnumFmtEtc.htm
tech.root: shell
ms.assetid: c391c8c8-6062-4e70-9a1f-de0eb610250d
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: SHCreateStdEnumFmtEtc, SHCreateStdEnumFmtEtc function [Windows Shell], _win32_SHCreateStdEnumFmtEtc, shell.SHCreateStdEnumFmtEtc, shlobj_core/SHCreateStdEnumFmtEtc
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
req.lib: Shell32.lib
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shell32.dll
 - ext-ms-win-shell-shell32-l1-2-1.dll
 - Ext-MS-Win-Shell-Shell32-L1-2-2.dll
 - windows.storage.dll
api_name:
 - SHCreateStdEnumFmtEtc
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- SHCreateStdEnumFmtEtc
: 
---

# SHCreateStdEnumFmtEtc function


## -description


<p class="CCE_Message">[<b>SHCreateStdEnumFmtEtc</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Creates an <a href="https://msdn.microsoft.com/4d180fdd-2d58-4d26-9242-6552dda0d3e6">IEnumFORMATETC</a> object from an array of <a href="https://msdn.microsoft.com/4478eb9a-84a1-4f3a-8290-94b8dd20c081">FORMATETC</a> structures.


## -parameters




### -param cfmt [in]

Type: <b>UINT</b>

The number of entries in the <i>afmt</i> array.


### -param afmt

Type: <b>const <a href="https://msdn.microsoft.com/4478eb9a-84a1-4f3a-8290-94b8dd20c081">FORMATETC</a>[]</b>

An array of <a href="https://msdn.microsoft.com/4478eb9a-84a1-4f3a-8290-94b8dd20c081">FORMATETC</a> structures that specifies the clipboard formats of interest.


### -param ppenumFormatEtc [out]

Type: <b><a href="https://msdn.microsoft.com/4d180fdd-2d58-4d26-9242-6552dda0d3e6">IEnumFORMATETC</a>**</b>

When this function returns successfully, receives an <a href="https://msdn.microsoft.com/4d180fdd-2d58-4d26-9242-6552dda0d3e6">IEnumFORMATETC</a> interface pointer. Receives <b>NULL</b> on failure.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



