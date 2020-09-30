---
UID: NF:winldap.ldap_get_valuesA
title: ldap_get_valuesA function (winldap.h)
description: The ldap_get_values function retrieves the list of values of a given attribute.
helpviewer_keywords: ["_ldap_ldap_get_values","ldap.ldap__get__values","ldap.ldap_get_values","ldap_get_values","ldap_get_values function [LDAP]","ldap_get_valuesA","ldap_get_valuesW","winldap/ldap_get_values","winldap/ldap_get_valuesA","winldap/ldap_get_valuesW"]
old-location: ldap\ldap_get_values.htm
tech.root: ldap
ms.assetid: a633afa1-4a37-4894-ae94-5225d99077fd
ms.date: 12/05/2018
ms.keywords: _ldap_ldap_get_values, ldap.ldap__get__values, ldap.ldap_get_values, ldap_get_values, ldap_get_values function [LDAP], ldap_get_valuesA, ldap_get_valuesW, winldap/ldap_get_values, winldap/ldap_get_valuesA, winldap/ldap_get_valuesW
req.header: winldap.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: ldap_get_valuesW (Unicode) and ldap_get_valuesA (ANSI)
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
 - ldap_get_valuesA
 - winldap/ldap_get_valuesA
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
 - ldap_get_values
 - ldap_get_valuesA
 - ldap_get_valuesW
---

# ldap_get_valuesA function


## -description

The <b>ldap_get_values</b> function retrieves the list of values of a given attribute.

## -parameters

### -param ld [in]

The session handle.

### -param entry [in]

The entry from which to retrieve values.

### -param attr [in]

A pointer to a null-terminated string that contains the attribute whose values are to be retrieved.

## -returns

If the function succeeds, it returns a null-terminated list of pointers to values. If no attribute values were found, it usually returns <b>NULL</b>. But in some cases it may return a list one pointer that is <b>NULL</b>. Always make sure to use <a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_count_values">ldap_count_values</a> to get the count of values in the returned list, as noted in Remarks. The session error parameter in the LDAP data structure is set to 0 in either case.

If the function fails, it returns <b>NULL</b> and the session error parameter in the LDAP data structure is set to the LDAP error code.

## -remarks

Use <b>ldap_get_values</b> when parsing a search response to obtain the value or values of an attribute. Use this function only when the attribute contains null-terminated character strings; for binary data, use 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_get_values_len">ldap_get_values_len</a> instead.

The entry is obtained by calling 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_first_entry">ldap_first_entry</a> or 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_next_entry">ldap_next_entry</a>. The attribute should be one returned by a call to 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_first_attribute">ldap_first_attribute</a>, 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_next_attribute">ldap_next_attribute</a>, or a caller-supplied string (for example, "mail").

Use <a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_count_values">ldap_count_values</a> to get the count of values in the returned list.
Call 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_value_free">ldap_value_free</a> to release the returned value when it is no longer required.

Certain LDAP servers place limits on the number of attribute string values that are returned in a single call.  For more information about using range retrieval specifiers, see <a href="/previous-versions/windows/desktop/ldap/searching-using-range-retrieval">Searching Using Range Retrieval</a>.

## -see-also

<a href="/previous-versions/windows/desktop/ldap/functions">Functions</a>



<a href="/previous-versions/windows/desktop/ldap/searching-a-directory">Searching a Directory</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_first_attribute">ldap_first_attribute</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_first_entry">ldap_first_entry</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_get_values_len">ldap_get_values_len</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_next_attribute">ldap_next_attribute</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_next_entry">ldap_next_entry</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_value_free">ldap_value_free</a>