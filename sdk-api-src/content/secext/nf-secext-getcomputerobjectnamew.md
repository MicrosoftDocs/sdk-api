---
UID: NF:secext.GetComputerObjectNameW
title: GetComputerObjectNameW function (secext.h)
description: Retrieves the local computer's name in a specified format.
helpviewer_keywords: ["GetComputerObjectName","GetComputerObjectName function","GetComputerObjectNameA","GetComputerObjectNameW","_win32_getcomputerobjectname","base.getcomputerobjectname","secext/GetComputerObjectName","secext/GetComputerObjectNameA","secext/GetComputerObjectNameW"]
old-location: base\getcomputerobjectname.htm
tech.root: SysInfo
ms.assetid: aead19ae-a27c-486e-aa2e-220d337044fc
ms.date: 12/05/2018
ms.keywords: GetComputerObjectName, GetComputerObjectName function, GetComputerObjectNameA, GetComputerObjectNameW, _win32_getcomputerobjectname, base.getcomputerobjectname, secext/GetComputerObjectName, secext/GetComputerObjectNameA, secext/GetComputerObjectNameW
f1_keywords:
- secext/GetComputerObjectName
dev_langs:
- c++
req.header: secext.h
req.include-header: Security.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: GetComputerObjectNameW (Unicode) and GetComputerObjectNameA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Secur32.lib
req.dll: Secur32.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- Secur32.dll
- Ext-MS-Win-secur32-translatename-l1-1-0.dll
- Ext-MS-Win-Secur32-Translatename-L1-1-1.dll
api_name:
- GetComputerObjectName
- GetComputerObjectNameA
- GetComputerObjectNameW
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# GetComputerObjectNameW function


## -description


Retrieves the local computer's name in a specified format.


## -parameters




### -param NameFormat [in]

The format for the name. This parameter is a value from the 
<a href="https://docs.microsoft.com/windows/desktop/api/secext/ne-secext-extended_name_format">EXTENDED_NAME_FORMAT</a> enumeration type. It cannot be NameUnknown.


### -param lpNameBuffer [out]

A pointer to a buffer that receives the name in the specified format. 




If this parameter is <b>NULL</b>, either the function succeeds and the <i>lpnSize</i> parameter receives the required size, or the function fails with ERROR_INSUFFICIENT_BUFFER and <i>lpnSize</i> receives the required size. The behavior depends on the value of <i>NameFormat</i> and the version of the operating system.


### -param nSize [in, out]

On input, specifies the size of the <i>lpNameBuffer</i> buffer, in <b>TCHARs</b>. On success, receives the size of the name copied to the buffer. If the <i>lpNameBuffer</i> buffer is too small to hold the name, the function fails and <i>lpnSize</i> receives the required buffer size.


## -returns



If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/secext/ne-secext-extended_name_format">EXTENDED_NAME_FORMAT</a>



<a href="https://docs.microsoft.com/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getcomputernameexa">GetComputerNameEx</a>



<a href="https://docs.microsoft.com/windows/desktop/SysInfo/system-information-functions">System
		  Information Functions</a>
 

 

