---
UID: NF:winldap.ldap_get_paged_count
title: ldap_get_paged_count function (winldap.h)
description: Records the number of paged results that the server has returned for a search.
helpviewer_keywords: ["_ldap_ldap_get_paged_count","ldap.ldap__get__paged__count","ldap.ldap_get_paged_count","ldap_get_paged_count","ldap_get_paged_count function [LDAP]","winldap/ldap_get_paged_count"]
old-location: ldap\ldap_get_paged_count.htm
tech.root: ldap
ms.assetid: 17ad1c7e-c3a1-4f6a-8303-fbbedfc36409
ms.date: 12/05/2018
ms.keywords: _ldap_ldap_get_paged_count, ldap.ldap__get__paged__count, ldap.ldap_get_paged_count, ldap_get_paged_count, ldap_get_paged_count function [LDAP], winldap/ldap_get_paged_count
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
 - ldap_get_paged_count
 - winldap/ldap_get_paged_count
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
 - ldap_get_paged_count
---

# ldap_get_paged_count function


## -description

The <b>ldap_get_paged_count</b> function records the number of paged results that the server has returned for a search.

## -parameters

### -param ExternalHandle [in]

The session handle.

### -param SearchBlock [in]

Handle to an 
<a href="/previous-versions/windows/desktop/legacy/aa366129(v=vs.85)">LDAPSearch</a> structure.

### -param TotalCount [out]

The total pages in the search results.

### -param Results [out]

A pointer to the 
<a href="/windows/desktop/api/winldap/ns-winldap-ldapmessage">LDAPMessage</a> structure that contains the results of the operation.

## -returns

If the function succeeds, the return value is <b>LDAP_SUCCESS</b>.

If the function fails, it returns an error code. For more information, see 
<a href="/previous-versions/windows/desktop/ldap/return-values">Return Values</a>.

## -remarks

Call <b>ldap_get_paged_count</b> for each  result set received after calling 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_get_next_page">ldap_get_next_page</a>. This allows the LDAP runtime to save from the cookie that the server uses to track  the search.

If you call 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_get_next_page_s">ldap_get_next_page_s</a>, a call to <b>ldap_get_paged_count</b> is not required.

## -see-also

<a href="/previous-versions/windows/desktop/ldap/functions">Functions</a>


<a href="/windows/desktop/api/winldap/ns-winldap-ldapmessage">LDAPMessage</a>


<a href="/previous-versions/windows/desktop/legacy/aa366129(v=vs.85)">LDAPSearch</a>



<a href="/previous-versions/windows/desktop/ldap/return-values">Return Values</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_get_next_page">ldap_get_next_page</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_get_next_page_s">ldap_get_next_page_s</a>