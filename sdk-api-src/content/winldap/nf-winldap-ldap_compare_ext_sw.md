---
UID: NF:winldap.ldap_compare_ext_sW
title: ldap_compare_ext_sW function (winldap.h)
description: The ldap_compare_ext_sW (Unicode) function (winldap.h) determines if an attribute, for a given entry, holds a known value.
helpviewer_keywords: ["_ldap_ldap_compare_ext_s", "ldap.ldap__compare__ext__s", "ldap.ldap_compare_ext_s", "ldap_compare_ext_s", "ldap_compare_ext_s function [LDAP]", "ldap_compare_ext_sW", "winldap/ldap_compare_ext_s", "winldap/ldap_compare_ext_sW"]
old-location: ldap\ldap_compare_ext_s.htm
tech.root: ldap
ms.assetid: b22568b1-5043-422e-9c4e-cc51cc77d143
ms.date: 08/08/2022
ms.keywords: _ldap_ldap_compare_ext_s, ldap.ldap__compare__ext__s, ldap.ldap_compare_ext_s, ldap_compare_ext_s, ldap_compare_ext_s function [LDAP], ldap_compare_ext_sA, ldap_compare_ext_sW, winldap/ldap_compare_ext_s, winldap/ldap_compare_ext_sA, winldap/ldap_compare_ext_sW
req.header: winldap.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: ldap_compare_ext_sW (Unicode) and ldap_compare_ext_sA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wldap32.lib
req.dll: Wldap32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ldap_compare_ext_sW
 - winldap/ldap_compare_ext_sW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wldap32.dll
api_name:
 - ldap_compare_ext_s
 - ldap_compare_ext_sA
 - ldap_compare_ext_sW
---

# ldap_compare_ext_sW function


## -description

Use the <b>ldap_compare_ext_s</b> function to determine if an attribute, for a given entry, holds a known value.

## -parameters

### -param ld [in]

The session handle.

### -param dn [in]

A pointer to a null-terminated string that contains the distinguished name of the entry to compare.

### -param Attr [in]

A pointer to a null-terminated string that contains the attribute to compare.

### -param Value [in]

A pointer to a null-terminated string that contains the string attribute value to be compared to the attribute value. Set to <b>NULL</b> if not used.

### -param Data [in]

The 
<a href="/windows/win32/api/winldap/ns-winldap-ldap_berval">berval</a> attribute value to be compared to the attribute value. Set to <b>NULL</b> if not used.

### -param ServerControls [in]

Optional. A list of LDAP server controls. Set to <b>NULL</b> if not used.

### -param ClientControls [in]

Optional. A list of LDAP client controls. Set to <b>NULL</b> if not used.

## -returns

If the function succeeds, and the attribute and known values match, <b>LDAP_COMPARE_TRUE</b> is returned; if the values do not match, <b>LDAP_COMPARE_FALSE</b> is returned.

If the function fails, an error code is returned. For more information, see 
<a href="/previous-versions/windows/desktop/ldap/return-values">Return Values</a>.

## -remarks

The <b>ldap_compare_ext_s</b> function initiates a synchronous compare operation, comparing the value of an attribute to a known value. The parameters and effects of <b>ldap_compare_ext_s</b> subsume those of 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_compare_s">ldap_compare_s</a>. The extended routine includes additional parameters to support client and server controls, and comparison of binary values.

Use the <i>Value</i> parameter for comparing string values or use the <i>Data</i> parameter for comparing raw binary data. Set the unused parameter to <b>NULL</b>. If neither parameter is <b>NULL</b>, the compare operation will use the value in the <i>Data</i> parameter.

Multithreading: Calls to <b>ldap_compare_ext_s</b> are thread-safe.





> [!NOTE]
> The winldap.h header defines ldap_compare_ext_s as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/previous-versions/windows/desktop/ldap/extended-controls">Extended Controls</a>



<a href="/previous-versions/windows/desktop/ldap/functions">Functions</a>



<a href="/previous-versions/windows/desktop/ldap/return-values">Return Values</a>



<a href="/previous-versions/windows/desktop/ldap/using-controls">Using Controls</a>



<a href="/windows/win32/api/winldap/ns-winldap-ldap_berval">berval</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_compare_s">ldap_compare_s</a>
