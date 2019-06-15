---
UID: NF:secext.TranslateNameA
title: TranslateNameA function (secext.h)
author: windows-sdk-content
description: Converts a directory service object name from one format to another.
old-location: base\translatename.htm
tech.root: SysInfo
ms.assetid: 4df25519-e7d6-46ea-b0e8-ba1f82e5f94f
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: TranslateName, TranslateName function, TranslateNameA, TranslateNameW, _win32_translatename, base.translatename, secext/TranslateName, secext/TranslateNameA, secext/TranslateNameW
ms.topic: function
f1_keywords: ["secext/TranslateName"]
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# TranslateNameA function


## -description


Converts a directory service object name from one format to another.


## -parameters




### -param lpAccountName [in]

The name to be translated.


### -param AccountNameFormat [in]

The format of the name to be translated. This parameter is a value from the 
<a href="https://docs.microsoft.com/windows/desktop/api/secext/ne-secext-extended_name_format">EXTENDED_NAME_FORMAT</a> enumeration type.


### -param DesiredNameFormat [in]

The format of the converted name. This parameter is a value from the 
<a href="https://docs.microsoft.com/windows/desktop/api/secext/ne-secext-extended_name_format">EXTENDED_NAME_FORMAT</a> enumeration type. It cannot be NameUnknown.


### -param lpTranslatedName [out]

A pointer to a buffer that receives the converted name.


### -param nSize [in, out]

On input, the variable indicates the size of the <i>lpTranslatedName</i> buffer, in <b>TCHARs</b>. On output, the variable returns the size of the returned string, in <b>TCHARs</b>, including the terminating <b>null</b> character. 




If <i>lpTranslated</i> is <b>NULL</b> and <i>nSize</i> is 0, the function succeeds and <i>nSize</i> receives the required buffer size.

If the <i>lpTranslatedName</i> buffer is too small to hold the converted name, the function fails and <i>nSize</i> receives the required buffer size.


## -returns



If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.




## -remarks



<b>TranslateName</b> fails if it cannot bind to Active Directory on a domain controller.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/SysInfo/computer-names">Computer Names</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ntdsapi/nf-ntdsapi-dscracknamesa">DsCrackNames</a>



<a href="https://docs.microsoft.com/windows/desktop/api/secext/ne-secext-extended_name_format">EXTENDED_NAME_FORMAT</a>



<a href="https://docs.microsoft.com/windows/desktop/SysInfo/system-information-functions">System Information Functions</a>
 

 

