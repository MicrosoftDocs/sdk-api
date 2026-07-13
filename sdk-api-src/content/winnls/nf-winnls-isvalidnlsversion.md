---
UID: NF:winnls.IsValidNLSVersion
title: IsValidNLSVersion function (winnls.h)
description: Determines if the NLS version is valid for a given NLS function.
helpviewer_keywords: ["IsValidNLSVersion","IsValidNLSVersion function [Internationalization for Windows Applications]","intl.isvalidnlsversion","winnls/IsValidNLSVersion"]
old-location: intl\isvalidnlsversion.htm
tech.root: Intl
ms.assetid: 29556DB4-E569-4161-9E47-149E4C12DD3B
ms.date: 12/05/2018
ms.keywords: IsValidNLSVersion, IsValidNLSVersion function [Internationalization for Windows Applications], intl.isvalidnlsversion, winnls/IsValidNLSVersion
req.header: winnls.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IsValidNLSVersion
 - winnls/IsValidNLSVersion
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-localization-l1-2-4.dll
 - api-ms-win-core-localization-l1-2-3.dll
 - Kernel32.dll
 - API-MS-Win-Core-Localization-l1-2-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-Localization-l1-2-1.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-Localization-L1-2-2.dll
api_name:
 - IsValidNLSVersion
---

# IsValidNLSVersion function


## -description

Determines if the NLS version is valid for a given NLS function.

## -parameters

### -param function [in]

The NLS capability to query. This value must be COMPARE_STRING. See the <a href="/windows/desktop/api/winnls/ne-winnls-sysnls_function">SYSNLS_FUNCTION</a> enumeration.

### -param lpLocaleName [in, optional]

Pointer to a <a href="/windows/desktop/Intl/locale-names">locale name</a>, or one of the following predefined values. 

<ul>
<li>
<a href="/windows/desktop/Intl/locale-name-constants">LOCALE_NAME_INVARIANT</a>
</li>
<li>
<a href="/windows/desktop/Intl/locale-name-constants">LOCALE_NAME_SYSTEM_DEFAULT</a>
</li>
<li>
<a href="/windows/desktop/Intl/locale-name-constants">LOCALE_NAME_USER_DEFAULT</a>
</li>
</ul>

### -param lpVersionInformation [in]

Pointer to an <a href="/windows/desktop/api/winnls/ns-winnls-nlsversioninfoex">NLSVERSIONINFOEX</a> structure. The application must initialize the <b>dwNLSVersionInfoSize</b> member to <code> sizeof(NLSVERSIONINFOEX)</code>.

## -returns

Returns a nonzero value if the NLS version is valid, or zero if the version is invalid.

## -remarks

Initialize the <a href="/windows/desktop/api/winnls/ns-winnls-nlsversioninfoex">NLSVERSIONINFOEX</a> structure by calling <a href="/windows/desktop/api/winnls/nf-winnls-getnlsversionex">GetNLSVersionEx</a>. See the Remarks for <b>GetNLSVersionEx</b> for a discussion on how the members of <b>NLSVERSIONINFOEX</b> can be used to determine if a sort version has changed and you need to reindex data.

<b>Beginning in Windows 8:</b> If your app passes language tags to this function from the <a href="/uwp/api/Windows.Globalization">Windows.Globalization</a> namespace, it must first convert the tags by calling <a href="/windows/desktop/api/winnls/nf-winnls-resolvelocalename">ResolveLocaleName</a>.

## -see-also

<b></b>



<a href="/windows/desktop/api/winnls/nf-winnls-getnlsversionex">GetNLSVersionEx</a>



<a href="/windows/desktop/Intl/handling-sorting-in-your-applications">Handling Sorting in Your Applications</a>



<a href="/windows/desktop/api/winnls/ns-winnls-nlsversioninfoex">NLSVERSIONINFOEX</a>