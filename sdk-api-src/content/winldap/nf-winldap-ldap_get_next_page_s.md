---
UID: NF:winldap.ldap_get_next_page_s
title: ldap_get_next_page_s function (winldap.h)
description: Returns the next page in a sequence of synchronous paged search results.
helpviewer_keywords: ["_ldap_ldap_get_next_page_s","ldap.ldap__get__next__page__s","ldap.ldap_get_next_page_s","ldap_get_next_page_s","ldap_get_next_page_s function [LDAP]","winldap/ldap_get_next_page_s"]
old-location: ldap\ldap_get_next_page_s.htm
tech.root: ldap
ms.assetid: 44b1b298-9796-4627-945e-4051c20f3c92
ms.date: 12/05/2018
ms.keywords: _ldap_ldap_get_next_page_s, ldap.ldap__get__next__page__s, ldap.ldap_get_next_page_s, ldap_get_next_page_s, ldap_get_next_page_s function [LDAP], winldap/ldap_get_next_page_s
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
 - ldap_get_next_page_s
 - winldap/ldap_get_next_page_s
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
 - ldap_get_next_page_s
---

# ldap_get_next_page_s function


## -description

The <b>ldap_get_next_page_s</b> function returns the next page in a sequence of synchronous paged search results.

## -parameters

### -param ExternalHandle [in]

Session handle.

### -param SearchHandle [in]

Search block handle.

### -param timeout [in]

The time value, in seconds, that the client will wait for the call to return.

### -param PageSize [in]

The number of entries to return in a single page.

### -param TotalCount [out]

The server estimate of the total number of entries in the entire result set. A value of zero indicates that the server cannot provide an estimate.

### -param Results [out]

A pointer to the 
<a href="/windows/win32/api/winldap/ns-winldap-ldapmessage">LDAPMessage</a> structure that contains the results.

## -returns

If the server returns a null cookie (non-continuation), the value is <b>LDAP_NO_RESULTS_RETURNED</b>. Otherwise, the client signals a continuation (more data available) by returning <b>LDAP_SUCCESS</b>.

If the function otherwise fails, it returns the error code return value related to the failure. For more information, see 
<a href="/previous-versions/windows/desktop/ldap/return-values">Return Values</a>.

## -remarks

The <b>ldap_get_next_page_s</b> function is part of the interface for simple, synchronous paging of search results. Use the search handle returned from an initial call to 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_search_init_page">ldap_search_init_page</a> and specify, in the <i>PageSize</i> parameter, the number of entries to be returned in a page. Set <i>PageSize</i> to zero to quit a search.

The results returned from <b>ldap_get_next_page_s</b> can be handled as any other search result, and should be freed, when finished, by calling 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_msgfree">ldap_msgfree</a>.

When parsing the results set, it is possible for the server to return an empty page of results and yet still respond with an <b>LDAP_SUCCESS</b> return code. This indicates that the server was unable to retrieve a page of results, due to a timeout or other reason,  but has not completed  the search request. The proper behavior in this instance is to continue to call <b>ldap_get_next_page_s</b> until either another page of results are successfully retrieved, an error code is returned, or <b>LDAP_NO_RESULTS_RETURNED</b> is returned to indicate the search is complete.

To retrieve paged search result asynchronously, use 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_get_next_page">ldap_get_next_page</a>.

If <b>ldap_get_next_page_s</b> is used, it is not required that 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_get_paged_count">ldap_get_paged_count</a> is called to record the number of paged results returned by a server.

## -see-also

<a href="/previous-versions/windows/desktop/ldap/functions">Functions</a>



<a href="/windows/win32/api/winldap/ns-winldap-ldapmessage">LDAPMessage</a>



<a href="/previous-versions/windows/desktop/ldap/return-values">Return Values</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_get_next_page">ldap_get_next_page</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_get_paged_count">ldap_get_paged_count</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_msgfree">ldap_msgfree</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_search_init_page">ldap_search_init_page</a>

