---
UID: NF:winldap.ldap_compare_extW
title: ldap_compare_extW function (winldap.h)
description: Use the ldap_compare_ext function to determine if an attribute, for a given entry, holds a known value.
helpviewer_keywords: ["_ldap_ldap_compare_ext","ldap.ldap__compare__ext","ldap.ldap_compare_ext","ldap_compare_ext","ldap_compare_ext function [LDAP]","ldap_compare_extA","ldap_compare_extW","winldap/ldap_compare_ext","winldap/ldap_compare_extA","winldap/ldap_compare_extW"]
old-location: ldap\ldap_compare_ext.htm
tech.root: ldap
ms.assetid: 07e96a95-439b-4bb1-a9ca-d76d181e8bea
ms.date: 12/05/2018
ms.keywords: _ldap_ldap_compare_ext, ldap.ldap__compare__ext, ldap.ldap_compare_ext, ldap_compare_ext, ldap_compare_ext function [LDAP], ldap_compare_extA, ldap_compare_extW, winldap/ldap_compare_ext, winldap/ldap_compare_extA, winldap/ldap_compare_extW
req.header: winldap.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: ldap_compare_extW (Unicode) and ldap_compare_extA (ANSI)
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
 - ldap_compare_extW
 - winldap/ldap_compare_extW
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
 - ldap_compare_ext
 - ldap_compare_extA
 - ldap_compare_extW
---

# ldap_compare_extW function


## -description

Use the <b>ldap_compare_ext</b> function to determine if an attribute, for a given entry, holds a known value.

## -parameters

### -param ld [in]

The session handle.

### -param dn [in]

A pointer to a null-terminated string that contains the distinguished name of the entry to compare.

### -param Attr [in]

A pointer to a null-terminated string that contains the attribute to compare.

### -param Value [in]

A pointer to a null-terminated string that contains the string attribute value to be compared to the attribute value.

### -param Data [in]

The 
<a href="/windows/win32/api/winldap/ns-winldap-ldap_berval">berval</a> attribute value to be compared to the attribute value.

### -param ServerControls [in]

Optional. A list of LDAP server controls. This parameter should be set to <b>NULL</b> if not used.

### -param ClientControls [in]

Optional. A list of client controls. This parameter should be set to <b>NULL</b> if not used.

### -param MessageNumber [out]

The message ID for the compare operation.

## -returns

If the function succeeds, <b>LDAP_SUCCESS</b> is returned.

If the function fails, an error code is returned. For more information, see 
<a href="/previous-versions/windows/desktop/ldap/return-values">Return Values</a> for more information.

## -remarks

The <b>ldap_compare_ext</b> function initiates an asynchronous compare operation, comparing the value of an attribute to a known value. The parameters and effects of <b>ldap_compare_ext</b> subsume those of 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_compare">ldap_compare</a>. The extended routine includes additional parameters to support client and server controls, comparison of binary values, and thread safety.

Use the <i>Value</i> parameter for comparing string values or use the <i>Data</i> parameter for comparing raw binary data. Set the unused parameter to <b>NULL</b>. If neither parameter is <b>NULL</b>, the compare operation will use the value in the <i>Data</i> parameter.

If successful, <b>ldap_compare_ext</b> passes back the message ID for the operation in the <i>MessageNumber</i> parameter. Call 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_result">ldap_result</a> with the message ID to obtain the result of the compare. To have the function return the compare result directly, use the synchronous extended compare function 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_compare_ext_s">ldap_compare_ext_s</a>.

Multithreading: Calls to <b>ldap_compare_ext</b> are thread-safe.





> [!NOTE]
> The winldap.h header defines ldap_compare_ext as an alias which automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/previous-versions/windows/desktop/ldap/extended-controls">Extended Controls</a>



<a href="/previous-versions/windows/desktop/ldap/functions">Functions</a>



<a href="/previous-versions/windows/desktop/ldap/return-values">Return Values</a>



<a href="/previous-versions/windows/desktop/ldap/using-controls">Using Controls</a>



<a href="/windows/win32/api/winldap/ns-winldap-ldap_berval">berval</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_compare">ldap_compare</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_compare_ext_s">ldap_compare_ext_s</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_result">ldap_result</a>