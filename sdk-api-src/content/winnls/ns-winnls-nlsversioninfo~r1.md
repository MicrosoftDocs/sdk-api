---
UID: NS:winnls._nlsversioninfo~r1
title: NLSVERSIONINFO
description: The NLSVERSIONINFO structure (winnls.h) is deprecated and should not be used.
ms.date: 08/19/2022
ms.keywords: _nlsversioninfo, NLSVERSIONINFO
targetos: Windows
req.construct-type: structure
req.ddi-compliance: 
req.dll: 
req.header: winnls.h
req.include-header: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.redist: 
req.target-min-winverclnt: Windows 10 Build 20348
req.target-min-winversvr: Windows 10 Build 20348
req.target-type: 
req.typenames: NLSVERSIONINFO, *LPNLSVERSIONINFO
req.umdf-ver: 
req.unicode-ansi: 
f1_keywords:
 - _nlsversioninfo
 - winnls/_nlsversioninfo
 - LPNLSVERSIONINFO
 - winnls/LPNLSVERSIONINFO
 - NLSVERSIONINFO
 - winnls/NLSVERSIONINFO
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - winnls.h
api_name:
 - _nlsversioninfo
 - NLSVERSIONINFO
---

# NLSVERSIONINFO structure


## -description

Deprecated. Contains version information about an NLS capability.



Starting with Windows 8, your app should use <a href="/windows/desktop/api/winnls/ns-winnls-nlsversioninfoex">NLSVERSIONINFOEX</a> instead of <b>NLSVERSIONINFO</b>.

## -struct-fields

### -field dwNLSVersionInfoSize

Size, in bytes, of the structure.

### -field dwNLSVersion

NLS version. This value is used to track changes and additions to the set of code points that have the indicated capability for a particular locale. The value is locale-specific, and increments when the capability changes. For example, using the COMPARE_STRING capability defined by the <a href="/windows/desktop/api/winnls/ne-winnls-sysnls_function">SYSNLS_FUNCTION</a> enumeration, the version changes if sorting weights are assigned to code points that previously had no weights defined for the locale.

### -field dwDefinedVersion

Defined version. This value is used to track changes in the repertoire of Unicode code points. The value increments when the Unicode repertoire is extended, for example, if more characters are defined.

## -remarks

Starting with Windows 8, <b>NLSVERSIONINFO</b> is deprecated. In fact, it is identical to <a href="/windows/desktop/api/winnls/ns-winnls-nlsversioninfoex">NLSVERSIONINFOEX</a>, which your app should use instead.

See Remarks for <a href="/windows/desktop/api/winnls/ns-winnls-nlsversioninfoex">NLSVERSIONINFOEX</a>.

## -see-also

<a href="/windows/desktop/api/winnls/nf-winnls-getnlsversion">GetNLSVersion</a>

<a href="/windows/desktop/api/winnls/nf-winnls-getnlsversionex">GetNLSVersionEx</a>

<a href="/windows/desktop/Intl/handling-sorting-in-your-applications">Handling Sorting in Your Applications</a>

<a href="/windows/desktop/api/winnls/nf-winnls-isnlsdefinedstring">IsNLSDefinedString</a>

<a href="/windows/desktop/api/winnls/ns-winnls-nlsversioninfoex">NLSVERSIONINFOEX</a>

<a href="/windows/desktop/Intl/national-language-support-structures">National Language Support Structures</a>
