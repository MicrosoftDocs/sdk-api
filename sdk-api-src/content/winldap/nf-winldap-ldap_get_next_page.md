---
UID: NF:winldap.ldap_get_next_page
title: ldap_get_next_page function (winldap.h)
description: Returns the next page in a sequence of asynchronous paged search results.
helpviewer_keywords: ["_ldap_ldap_get_next_page","ldap.ldap__get__next__page","ldap.ldap_get_next_page","ldap_get_next_page","ldap_get_next_page function [LDAP]","winldap/ldap_get_next_page"]
old-location: ldap\ldap_get_next_page.htm
tech.root: ldap
ms.assetid: 34ddf4d4-3a89-42e0-850d-fcc1c942cb3b
ms.date: 12/05/2018
ms.keywords: _ldap_ldap_get_next_page, ldap.ldap__get__next__page, ldap.ldap_get_next_page, ldap_get_next_page, ldap_get_next_page function [LDAP], winldap/ldap_get_next_page
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
 - ldap_get_next_page
 - winldap/ldap_get_next_page
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
 - ldap_get_next_page
---

# ldap_get_next_page function


## -description

The <b>ldap_get_next_page</b> function returns the next page in a sequence of asynchronous paged search results.

## -parameters

### -param ExternalHandle [in]

Session handle.

### -param SearchHandle [in]

Search block handle.

### -param PageSize [in]

The number of entries to return in a single page.

### -param MessageNumber [out]

The message ID for the request.

## -returns

If the function succeeds, the return value is <b>LDAP_SUCCESS</b>.

If the function fails, it returns an error code return value. For more information, see 
<a href="/previous-versions/windows/desktop/ldap/return-values">Return Values</a>.

## -remarks

The <b>ldap_get_next_page</b> function is part of the interface for simple, asynchronous paging of search results. Use the search handle returned from an initial call to 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_search_init_page">ldap_search_init_page</a> and specify, in the <i>PageSize</i> parameter, the number of entries to be returned in a page. Set <i>PageSize</i> to zero to abandon a search.

Be aware that after each call to <b>ldap_get_next_page</b>, you must call 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_get_paged_count">ldap_get_paged_count</a> for each set of results returned from the server using <a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_result">ldap_result</a>. This enables the LDAP run time to save the cookie that the server passed back to maintain the search state. Other than calling <b>ldap_get_paged_count</b>, the results returned from <b>ldap_get_next_page</b> can be handled as any other search result, and must be freed when complete by calling 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_msgfree">ldap_msgfree</a>.

When parsing the results set, be aware that it is possible for the server to return an empty page of results and yet still respond with an <b>LDAP_SUCCESS</b> return value. This indicates that the server was unable to retrieve a page of results, due to a timeout or other reason,  but has not finished the search request. The proper behavior, in this instance, is to continue to call <b>ldap_get_next_page</b> until either another page of results are successfully retrieved, an error code is returned, or <b>LDAP_NO_RESULTS_RETURNED</b> is returned to indicate that the search is complete.

If you prefer to retrieve paged search results synchronously, use 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_get_next_page_s">ldap_get_next_page_s</a>.

## -see-also

<a href="/previous-versions/windows/desktop/ldap/functions">Functions</a>



<a href="/previous-versions/windows/desktop/api/winldap/ns-winldap-ldap">LDAP</a>



<a href="/previous-versions/windows/desktop/ldap/return-values">Return Values</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_get_next_page_s">ldap_get_next_page_s</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_get_paged_count">ldap_get_paged_count</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_msgfree">ldap_msgfree</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_result">ldap_result</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_search_init_page">ldap_search_init_page</a>