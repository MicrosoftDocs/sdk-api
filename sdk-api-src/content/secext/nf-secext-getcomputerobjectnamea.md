---
UID: NF:secext.GetComputerObjectNameA
title: GetComputerObjectNameA function (secext.h)
description: Retrieves the local computer's name in a specified format. (ANSI)
helpviewer_keywords: ["GetComputerObjectNameA", "secext/GetComputerObjectNameA"]
old-location: base\getcomputerobjectname.htm
tech.root: winprog
ms.assetid: aead19ae-a27c-486e-aa2e-220d337044fc
ms.date: 12/05/2018
ms.keywords: GetComputerObjectName, GetComputerObjectName function, GetComputerObjectNameA, GetComputerObjectNameW, _win32_getcomputerobjectname, base.getcomputerobjectname, secext/GetComputerObjectName, secext/GetComputerObjectNameA, secext/GetComputerObjectNameW
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GetComputerObjectNameA
 - secext/GetComputerObjectNameA
dev_langs:
 - c++
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
req.apiset: ext-ms-win-secur32-translatename-l1-1-0 (introduced in Windows 8)
---

# GetComputerObjectNameA function


## -description

Retrieves the local computer's name in a specified format.

## -parameters

### -param NameFormat [in]

The format for the name. This parameter is a value from the 
<a href="/windows/desktop/api/secext/ne-secext-extended_name_format">EXTENDED_NAME_FORMAT</a> enumeration type. It cannot be NameUnknown.

### -param lpNameBuffer [out]

A pointer to a buffer that receives the name in the specified format. 




If this parameter is <b>NULL</b>, either the function succeeds and the <i>lpnSize</i> parameter receives the required size, or the function fails with ERROR_INSUFFICIENT_BUFFER and <i>lpnSize</i> receives the required size. The behavior depends on the value of <i>NameFormat</i> and the version of the operating system.

### -param nSize [in, out]

On input, specifies the size of the <i>lpNameBuffer</i> buffer, in <b>TCHARs</b>. On success, receives the size of the name copied to the buffer. If the <i>lpNameBuffer</i> buffer is too small to hold the name, the function fails and <i>lpnSize</i> receives the required buffer size.

## -returns

If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -see-also

<a href="/windows/desktop/api/secext/ne-secext-extended_name_format">EXTENDED_NAME_FORMAT</a>



<a href="/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getcomputernameexa">GetComputerNameEx</a>



<a href="/windows/desktop/SysInfo/system-information-functions">System
		  Information Functions</a>

## -remarks

> [!NOTE]
> The secext.h header defines GetComputerObjectName as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
