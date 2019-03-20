---
UID: NF:shlobj_core.SHCLSIDFromString
title: SHCLSIDFromString function (shlobj_core.h)
author: windows-sdk-content
description: Takes the string form of a class identifier (CLSID) and creates the corresponding CLSID.
old-location: shell\SHCLSIDFromString.htm
tech.root: shell
ms.assetid: b09950fb-0a72-4829-aedd-cf01a3f98074
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: SHCLSIDFromString, SHCLSIDFromString function [Windows Shell], _win32_SHCLSIDFromString, shell.SHCLSIDFromString, shlobj_core/SHCLSIDFromString
ms.topic: function
req.header: shlobj_core.h
req.include-header: Shlobj.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
api_name:
 - SHCLSIDFromString
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SHCLSIDFromString function


## -description


<p class="CCE_Message">[This function is available through Windows XP Service Pack 2 (SP2) and Windows Server 2003. It might be altered or unavailable in subsequent versions of Windows. Use <a href="https://msdn.microsoft.com/36cc9037-480f-491f-a9bb-5aa1e707781e">CLSIDFromString</a> instead.]

Takes the string form of a class identifier (CLSID) and creates the corresponding CLSID.


## -parameters




### -param psz [in]

Type: <b>PCWSTR</b>

A Unicode string that contains the CLSID in the format, <code>{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}</code>.


### -param pclsid [out]

Type: <b>CLSID*</b>

A pointer to a CLSID value that, when this function returns successfully, receives the converted string as a CLSID.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



