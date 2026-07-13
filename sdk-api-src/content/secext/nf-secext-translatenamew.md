---
UID: NF:secext.TranslateNameW
title: TranslateNameW function (secext.h)
description: Converts a directory service object name from one format to another. (Unicode)
helpviewer_keywords: ["TranslateName", "TranslateName function", "TranslateNameW", "_win32_translatename", "base.translatename", "secext/TranslateName", "secext/TranslateNameW"]
old-location: base\translatename.htm
tech.root: winprog
ms.assetid: 4df25519-e7d6-46ea-b0e8-ba1f82e5f94f
ms.date: 12/05/2018
ms.keywords: TranslateName, TranslateName function, TranslateNameA, TranslateNameW, _win32_translatename, base.translatename, secext/TranslateName, secext/TranslateNameA, secext/TranslateNameW
req.header: secext.h
req.include-header: Security.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: TranslateNameW (Unicode) and TranslateNameA (ANSI)
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
 - TranslateNameW
 - secext/TranslateNameW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Secur32.dll
api_name:
 - TranslateName
 - TranslateNameA
 - TranslateNameW
req.apiset: ext-ms-win-secur32-translatename-l1-1-0 (introduced in Windows 8)
---

# TranslateNameW function


## -description

Converts a directory service object name from one format to another.

## -parameters

### -param lpAccountName [in]

The name to be translated.

### -param AccountNameFormat [in]

The format of the name to be translated. This parameter is a value from the 
<a href="/windows/desktop/api/secext/ne-secext-extended_name_format">EXTENDED_NAME_FORMAT</a> enumeration type.

### -param DesiredNameFormat [in]

The format of the converted name. This parameter is a value from the 
<a href="/windows/desktop/api/secext/ne-secext-extended_name_format">EXTENDED_NAME_FORMAT</a> enumeration type. It cannot be NameUnknown.

### -param lpTranslatedName [out]

A pointer to a buffer that receives the converted name.

### -param nSize [in, out]

On input, the variable indicates the size of the <i>lpTranslatedName</i> buffer, in <b>TCHARs</b>. On output, the variable returns the size of the returned string, in <b>TCHARs</b>, including the terminating <b>null</b> character. 




If <i>lpTranslated</i> is <b>NULL</b> and <i>nSize</i> is 0, the function succeeds and <i>nSize</i> receives the required buffer size.

If the <i>lpTranslatedName</i> buffer is too small to hold the converted name, the function fails and <i>nSize</i> receives the required buffer size.

## -returns

If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

<b>TranslateName</b> fails if it cannot bind to Active Directory on a domain controller.





> [!NOTE]
> The secext.h header defines TranslateName as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/SysInfo/computer-names">Computer Names</a>



<a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dscracknamesa">DsCrackNames</a>



<a href="/windows/desktop/api/secext/ne-secext-extended_name_format">EXTENDED_NAME_FORMAT</a>



<a href="/windows/desktop/SysInfo/system-information-functions">System Information Functions</a>
