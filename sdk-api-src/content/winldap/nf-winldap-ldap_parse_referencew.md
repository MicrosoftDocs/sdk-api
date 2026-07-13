---
UID: NF:winldap.ldap_parse_referenceW
title: ldap_parse_referenceW function (winldap.h)
description: The ldap_parse_referenceW (Unicode) function (winldap.h) returns a list of subordinate referrals in a search response message. 
helpviewer_keywords: ["_ldap_ldap_parse_reference", "ldap.ldap__parse__reference", "ldap.ldap_parse_reference", "ldap_parse_reference", "ldap_parse_reference function [LDAP]", "ldap_parse_referenceW", "winldap/ldap_parse_reference", "winldap/ldap_parse_referenceW"]
old-location: ldap\ldap_parse_reference.htm
tech.root: ldap
ms.assetid: 106db7dd-ee1e-48c9-9357-e14d4f8e8782
ms.date: 08/04/2022
ms.keywords: _ldap_ldap_parse_reference, ldap.ldap__parse__reference, ldap.ldap_parse_reference, ldap_parse_reference, ldap_parse_reference function [LDAP], ldap_parse_referenceA, ldap_parse_referenceW, winldap/ldap_parse_reference, winldap/ldap_parse_referenceA, winldap/ldap_parse_referenceW
req.header: winldap.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: ldap_parse_referenceW (Unicode) and ldap_parse_referenceA (ANSI)
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
 - ldap_parse_referenceW
 - winldap/ldap_parse_referenceW
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
 - ldap_parse_reference
 - ldap_parse_referenceA
 - ldap_parse_referenceW
---

# ldap_parse_referenceW function


## -description

The <b>ldap_parse_reference</b> function returns a list of subordinate referrals in a search response message.

## -parameters

### -param Connection [in]

The session handle.

### -param ResultMessage [in]

A pointer to an 
<a href="/windows/desktop/api/winldap/ns-winldap-ldapmessage">LDAPMessage</a> structure containing the search response.

### -param Referrals [out]

A pointer to the list of subordinate referrals. Free with <a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_value_free">ldap_value_free</a>.

## -returns

If the function succeeds, the return value is <b>LDAP_SUCCESS</b>.

If the function fails, it returns an error code. See 
<a href="/previous-versions/windows/desktop/ldap/return-values">Return Values</a> for more information.

## -remarks

The <b>ldap_parse_reference</b> function returns a list of referrals in the form of URLs. Call this function if a call to 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_parse_result">ldap_parse_result</a> indicates that there are referrals.

When it is no longer needed, free the <i>Referrals</i> pointer by calling 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_value_free">ldap_value_free</a>.




> [!NOTE]
> The winldap.h header defines ldap_parse_reference as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/previous-versions/windows/desktop/ldap/functions">Functions</a>



<a href="/windows/desktop/api/winldap/ns-winldap-ldapmessage">LDAPMessage</a>


<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_parse_result">ldap_parse_result</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_value_free">ldap_value_free</a>
