---
UID: NF:msacm.acmGetVersion
title: acmGetVersion function (msacm.h)
description: The acmGetVersion function returns the version number of the ACM.
helpviewer_keywords: ["_win32_acmGetVersion","acmGetVersion","acmGetVersion function [Windows Multimedia]","msacm/acmGetVersion","multimedia.acmgetversion"]
old-location: multimedia\acmgetversion.htm
tech.root: Multimedia
ms.assetid: 5a710149-0c3a-4dde-8069-db2e42826080
ms.date: 12/05/2018
ms.keywords: _win32_acmGetVersion, acmGetVersion, acmGetVersion function [Windows Multimedia], msacm/acmGetVersion, multimedia.acmgetversion
req.header: msacm.h
req.include-header: 
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
req.lib: Msacm32.lib
req.dll: Msacm32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - acmGetVersion
 - msacm/acmGetVersion
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Msacm32.dll
 - Ext-MS-Win-mm-msacm-l1-1-0.dll
api_name:
 - acmGetVersion
---

# acmGetVersion function


## -description

The <b>acmGetVersion</b> function returns the version number of the ACM.



## -returns

The version number is returned as a hexadecimal number of the form 0xAABBCCCC, where AA is the major version number, BB is the minor version number, and CCCC is the build number.

## -remarks

Win32 applications must verify that the ACM version is at least 0x03320000 (version 3.50) or greater before attempting to use any other ACM functions. The build number (CCCC) is always zero for the retail (non-debug) version of the ACM.

To display the ACM version for a user, an application should use the following format (note that the values should be printed as unsigned decimals):


```cpp

{ 
    DWORD   dw; 
    TCHAR   ach[10]; 
 
    dw = acmGetVersion(); 
    _stprintf_s(ach, TEXT("%u.%.02u"), 
        HIWORD(dw) >> 8, HIWORD(dw) & 0x00FF); 
} 

```

## -see-also

<a href="/windows/desktop/Multimedia/audio-compression-functions">Audio Compression Functions</a>



<a href="/windows/desktop/Multimedia/audio-compression-manager">Audio Compression Manager</a>
