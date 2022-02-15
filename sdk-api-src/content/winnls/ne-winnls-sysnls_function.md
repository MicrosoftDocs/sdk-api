---
UID: NE:winnls.SYSNLS_FUNCTION
title: SYSNLS_FUNCTION (winnls.h)
description: Specifies NLS function capabilities.
helpviewer_keywords: ["COMPARE_STRING","SYSNLS_FUNCTION","SYSNLS_FUNCTION enumeration [Internationalization for Windows Applications]","intl.nls_function","intl.sysnls_function","winnls/COMPARE_STRING","winnls/SYSNLS_FUNCTION"]
old-location: intl\sysnls_function.htm
tech.root: Intl
ms.assetid: c34eb904-e264-4f7d-ac7f-4ec8cfc588b6
ms.date: 12/05/2018
ms.keywords: COMPARE_STRING, SYSNLS_FUNCTION, SYSNLS_FUNCTION enumeration [Internationalization for Windows Applications], intl.nls_function, intl.sysnls_function, winnls/COMPARE_STRING, winnls/SYSNLS_FUNCTION
req.header: winnls.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SYSNLS_FUNCTION
 - winnls/SYSNLS_FUNCTION
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winnls.h
api_name:
 - SYSNLS_FUNCTION
---

# SYSNLS_FUNCTION enumeration


## -description

Specifies NLS function capabilities.

## -enum-fields

### -field COMPARE_STRING:0x0001

Value indicating comparison of two strings in the manner of the <a href="/windows/desktop/api/stringapiset/nf-stringapiset-comparestringw">CompareString</a> function or <a href="/windows/desktop/api/winnls/nf-winnls-lcmapstringa">LCMapString</a> with the LCMAP_SORTKEY flag specified.

## -see-also

<a href="/windows/desktop/api/stringapiset/nf-stringapiset-comparestringw">CompareString</a>



<a href="/windows/desktop/api/winnls/nf-winnls-getnlsversion">GetNLSVersion</a>



<a href="/windows/desktop/api/winnls/nf-winnls-isnlsdefinedstring">IsNLSDefinedString</a>



<a href="/windows/desktop/api/winnls/nf-winnls-lcmapstringa">LCMapString</a>



<a href="/windows/desktop/Intl/national-language-support-enumeration-types">National Language Support Enumeration Types</a>
