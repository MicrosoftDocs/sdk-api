---
UID: NF:winldap.ldap_get_values_lenW
title: ldap_get_values_lenW function (winldap.h)
description: The ldap_get_values_lenW (Unicode) function (winldap.h) retrieves the list of values for a given attribute. 
helpviewer_keywords: ["_ldap_ldap_get_values_len", "ldap.ldap__get__values__len", "ldap.ldap_get_values_len", "ldap_get_values_len", "ldap_get_values_len function [LDAP]", "ldap_get_values_lenW", "winldap/ldap_get_values_len", "winldap/ldap_get_values_lenW"]
old-location: ldap\ldap_get_values_len.htm
tech.root: ldap
ms.assetid: e2100892-5dad-4fc7-8129-34c675bcf134
ms.date: 08/03/2022
ms.keywords: _ldap_ldap_get_values_len, ldap.ldap__get__values__len, ldap.ldap_get_values_len, ldap_get_values_len, ldap_get_values_len function [LDAP], ldap_get_values_lenA, ldap_get_values_lenW, winldap/ldap_get_values_len, winldap/ldap_get_values_lenA, winldap/ldap_get_values_lenW
req.header: winldap.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: ldap_get_values_lenW (Unicode) and ldap_get_values_lenA (ANSI)
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
 - ldap_get_values_lenW
 - winldap/ldap_get_values_lenW
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
 - ldap_get_values_len
 - ldap_get_values_lenA
 - ldap_get_values_lenW
---

# ldap_get_values_lenW function


## -description

The <b>ldap_get_values_len</b> function retrieves the list of values for a given attribute.

## -parameters

### -param ExternalHandle [in]

The session handle.

### -param Message [in]

Handle to the 
<a href="/windows/desktop/api/winldap/ns-winldap-ldapmessage">LDAPMessage</a> structure.

### -param attr [in]

A pointer to a null-terminated string that contains the attribute whose values are to be retrieved.

## -returns

If the function succeeds, it returns a null-terminated list of pointers to 
<a href="/windows/win32/api/winldap/ns-winldap-ldap_berval">berval</a> structures that contain the values of the specified attribute. If no attribute values were found, it returns <b>NULL</b>. The session error parameter in the LDAP data structure is set to 0 in either case.

If the function fails, it returns <b>NULL</b> and the session error parameter in the LDAP data structure is set to the LDAP error code.

## -remarks

Use <b>ldap_get_values_len</b> when parsing a search response to obtain the value or values of an attribute. Use this function when the attribute contains binary data; for attributes whose values are null-terminated character strings, use 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_get_values">ldap_get_values</a>.

The entry is obtained by calling 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_first_entry">ldap_first_entry</a> or 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_next_entry">ldap_next_entry</a>. The attribute should be one returned by a call to 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_first_attribute">ldap_first_attribute</a>, 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_next_attribute">ldap_next_attribute</a>, or a caller-supplied string (for example, "mail").

Call 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_value_free_len">ldap_value_free_len</a> to release the returned value when it is no longer required.





> [!NOTE]
> The winldap.h header defines ldap_get_values_len as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/previous-versions/windows/desktop/ldap/functions">Functions</a>



<a href="/windows/desktop/api/winldap/ns-winldap-ldapmessage">LDAPMessage</a>



<a href="/windows/win32/api/winldap/ns-winldap-ldap_berval">berval</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_first_attribute">ldap_first_attribute</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_first_entry">ldap_first_entry</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_get_values">ldap_get_values</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_next_attribute">ldap_next_attribute</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_next_entry">ldap_next_entry</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_value_free_len">ldap_value_free_len</a>
