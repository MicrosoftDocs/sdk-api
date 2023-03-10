---
UID: NF:winldap.ldap_first_reference
title: ldap_first_reference function (winldap.h)
description: Returns the first reference from a message.
helpviewer_keywords: ["_ldap_ldap_first_reference","ldap.ldap__first__reference","ldap.ldap_first_reference","ldap_first_reference","ldap_first_reference function [LDAP]","winldap/ldap_first_reference"]
old-location: ldap\ldap_first_reference.htm
tech.root: ldap
ms.assetid: b9ee4da3-9309-4e2b-95a9-6e0f1625fc79
ms.date: 12/05/2018
ms.keywords: _ldap_ldap_first_reference, ldap.ldap__first__reference, ldap.ldap_first_reference, ldap_first_reference, ldap_first_reference function [LDAP], winldap/ldap_first_reference
req.header: winldap.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
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
 - ldap_first_reference
 - winldap/ldap_first_reference
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
 - ldap_first_reference
---

# ldap_first_reference function


## -description

The <b>ldap_first_reference</b> function returns the first reference from a message.

## -parameters

### -param ld [in]

The session handle.

### -param res [in]

The search result, as obtained by a call to one of the synchronous search routines or 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_result">ldap_result</a>.

## -returns

If the search returned valid results, this function returns a pointer to the first result reference. If no entry or reference exists in the result set, it returns <b>NULL</b>. This is the only error return; the session error parameter in the LDAP data structure is cleared to 0 in either case.

## -remarks

Use <b>ldap_first_reference</b> in conjunction with 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_next_reference">ldap_next_reference</a> to step through and retrieve a list of continuation references from a search result chain.

The function returns subordinate referrals (references) that are returned in search responses. A subordinate referral is one in which the server has returned some data and the referral has been passed to other naming contexts below the current level in the tree. To step through external references in which the naming context does not reside on the server, use 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_parse_result">ldap_parse_result</a> instead.

You do not have to explicitly free the returned reference as it is freed when the message itself is freed.

## -see-also

<a href="/previous-versions/windows/desktop/ldap/functions">Functions</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_next_reference">ldap_next_reference</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_parse_result">ldap_parse_result</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_result">ldap_result</a>