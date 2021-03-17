---
UID: NF:oleacc.GetOleaccVersionInfo
title: GetOleaccVersionInfo function (oleacc.h)
description: Retrieves the version number and build number of the Microsoft Active Accessibility file Oleacc.dll.
helpviewer_keywords: ["GetOleaccVersionInfo","GetOleaccVersionInfo function [Windows Accessibility]","_msaa_GetOleaccVersionInfo","msaa.getoleaccversioninfo","oleacc/GetOleaccVersionInfo","winauto.getoleaccversioninfo"]
old-location: winauto\getoleaccversioninfo.htm
tech.root: WinAuto
ms.assetid: 96dcdb85-4f35-4274-ba57-2f565c3ebb5f
ms.date: 12/05/2018
ms.keywords: GetOleaccVersionInfo, GetOleaccVersionInfo function [Windows Accessibility], _msaa_GetOleaccVersionInfo, msaa.getoleaccversioninfo, oleacc/GetOleaccVersionInfo, winauto.getoleaccversioninfo
req.header: oleacc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
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
req.lib: Oleacc.lib
req.dll: Oleacc.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: Active Accessibility 1.3 RDK on Windows NT 4.0 with SP6 and later and Windows 95
ms.custom: 19H1
f1_keywords:
 - GetOleaccVersionInfo
 - oleacc/GetOleaccVersionInfo
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Oleacc.dll
api_name:
 - GetOleaccVersionInfo
---

# GetOleaccVersionInfo function


## -description

Retrieves the version number and build number of the Microsoft Active Accessibility file Oleacc.dll.

## -parameters

### -param pVer [out]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a>*</b>

Address of a <b>DWORD</b> that receives the version number. The major version number is placed in the high word, and the minor version number is placed in the low word.

### -param pBuild [out]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a>*</b>

Address of a <b>DWORD</b> that receives the build number. The major build number is placed in the high word, and the minor build number is placed in the low word.

## -remarks

This function provides an easy way to get the version and build numbers for Oleacc.dll. The <a href="/windows/win32/api/winver/nf-winver-getfileversioninfosizea">GetFileVersionInfoSize</a>, <a href="/windows/win32/api/winver/nf-winver-getfileversioninfoa">GetFileVersionInfo</a>, and <a href="/windows/win32/api/winver/nf-winver-verqueryvaluea">VerQueryValue</a> functions can be used to retrieve the same information.