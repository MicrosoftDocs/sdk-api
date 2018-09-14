---
UID: NF:winldap.ldap_get_next_page_s
title: ldap_get_next_page_s function
author: windows-sdk-content
description: Returns the next page in a sequence of synchronous paged search results.
old-location: ldap\ldap_get_next_page_s.htm
tech.root: LDAP
ms.assetid: 44b1b298-9796-4627-945e-4051c20f3c92
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: "_ldap_ldap_get_next_page_s, ldap.ldap__get__next__page__s, ldap.ldap_get_next_page_s, ldap_get_next_page_s, ldap_get_next_page_s function [LDAP], winldap/ldap_get_next_page_s"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wldap32.dll
api_name:
 - ldap_get_next_page_s
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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
<a href="https://msdn.microsoft.com/547a0736-23a4-4bfd-8ae0-866825228b53">LDAPMessage</a> structure that contains the results.


## -returns



If the server returns a null cookie (non-continuation), the value is <b>LDAP_NO_RESULTS_RETURNED</b>. Otherwise, the client signals a continuation (more data available) by returning <b>LDAP_SUCCESS</b>.

If the function otherwise fails, it returns the error code return value related to the failure. For more information, see 
<a href="https://msdn.microsoft.com/822411b7-fc49-4b93-8e54-353350ed5de9">Return Values</a>.




## -remarks



The <b>ldap_get_next_page_s</b> function is part of the interface for simple, synchronous paging of search results. Use the search handle returned from an initial call to 
<a href="https://msdn.microsoft.com/f88d32e3-ac5f-4934-bf84-4007ffd72ac2">ldap_search_init_page</a> and specify, in the <i>PageSize</i> parameter, the number of entries to be returned in a page. Set <i>PageSize</i> to zero to quit a search.

The results returned from <b>ldap_get_next_page_s</b> can be handled as any other search result, and should be freed, when finished, by calling 
<a href="https://msdn.microsoft.com/a4292638-0686-4c2d-8c51-1d5d079d5782">ldap_msgfree</a>.

When parsing the results set, it is possible for the server to return an empty page of results and yet still respond with an <b>LDAP_SUCCESS</b> return code. This indicates that the server was unable to retrieve a page of results, due to a timeout or other reason,  but has not completed  the search request. The proper behavior in this instance is to continue to call <b>ldap_get_next_page_s</b> until either another page of results are successfully retrieved, an error code is returned, or <b>LDAP_NO_RESULTS_RETURNED</b> is returned to indicate the search is complete.

To retrieve paged search result asynchronously, use 
<a href="https://msdn.microsoft.com/34ddf4d4-3a89-42e0-850d-fcc1c942cb3b">ldap_get_next_page</a>.

If <b>ldap_get_next_page_s</b> is used, it is not required that 
<a href="https://msdn.microsoft.com/17ad1c7e-c3a1-4f6a-8303-fbbedfc36409">ldap_get_paged_count</a> is called to record the number of paged results returned by a server.




## -see-also




<a href="https://msdn.microsoft.com/7a0040ea-f8f3-4378-8371-49768714d762">Functions</a>



<a href="https://msdn.microsoft.com/547a0736-23a4-4bfd-8ae0-866825228b53">LDAPMessage</a>



<a href="https://msdn.microsoft.com/822411b7-fc49-4b93-8e54-353350ed5de9">Return Values</a>



<a href="https://msdn.microsoft.com/34ddf4d4-3a89-42e0-850d-fcc1c942cb3b">ldap_get_next_page</a>



<a href="https://msdn.microsoft.com/17ad1c7e-c3a1-4f6a-8303-fbbedfc36409">ldap_get_paged_count</a>



<a href="https://msdn.microsoft.com/a4292638-0686-4c2d-8c51-1d5d079d5782">ldap_msgfree</a>



<a href="https://msdn.microsoft.com/f88d32e3-ac5f-4934-bf84-4007ffd72ac2">ldap_search_init_page</a>
 

 

