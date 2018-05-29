---
UID: NF:winldap.ldap_get_next_page
title: ldap_get_next_page function
author: windows-sdk-content
description: Returns the next page in a sequence of asynchronous paged search results.
old-location: ldap\ldap_get_next_page.htm
old-project: LDAP
ms.assetid: 34ddf4d4-3a89-42e0-850d-fcc1c942cb3b
ms.author: windowssdkdev
ms.date: 05/15/2018
ms.keywords: "_ldap_ldap_get_next_page, ldap.ldap__get__next__page, ldap.ldap_get_next_page, ldap_get_next_page, ldap_get_next_page function [LDAP], winldap/ldap_get_next_page"
ms.prod: windows
ms.technology: windows-sdk
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
req.typenames: VOLUME_GET_GPT_ATTRIBUTES_INFORMATION, *PVOLUME_GET_GPT_ATTRIBUTES_INFORMATION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Wldap32.dll
api_name:
-	ldap_get_next_page
product: Windows
targetos: Windows
req.lib: Wldap32.lib
req.dll: Wldap32.dll
req.irql: 
req.product: Windows Address Book 5.0
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
<a href="https://msdn.microsoft.com/822411b7-fc49-4b93-8e54-353350ed5de9">Return Values</a>.




## -remarks



The <b>ldap_get_next_page</b> function is part of the interface for simple, asynchronous paging of search results. Use the search handle returned from an initial call to 
<a href="https://msdn.microsoft.com/f88d32e3-ac5f-4934-bf84-4007ffd72ac2">ldap_search_init_page</a> and specify, in the <i>PageSize</i> parameter, the number of entries to be returned in a page. Set <i>PageSize</i> to zero to abandon a search.

Be aware that after each call to <b>ldap_get_next_page</b>, you must call 
<a href="https://msdn.microsoft.com/17ad1c7e-c3a1-4f6a-8303-fbbedfc36409">ldap_get_paged_count</a> for each set of results returned from the server using <a href="https://msdn.microsoft.com/e047fccc-a875-4360-be1b-3ac3dea15dd6">ldap_result</a>. This enables the LDAP run time to save the cookie that the server passed back to maintain the search state. Other than calling <b>ldap_get_paged_count</b>, the results returned from <b>ldap_get_next_page</b> can be handled as any other search result, and must be freed when complete by calling 
<a href="https://msdn.microsoft.com/a4292638-0686-4c2d-8c51-1d5d079d5782">ldap_msgfree</a>.

When parsing the results set, be aware that it is possible for the server to return an empty page of results and yet still respond with an <b>LDAP_SUCCESS</b> return value. This indicates that the server was unable to retrieve a page of results, due to a timeout or other reason,  but has not finished the search request. The proper behavior, in this instance, is to continue to call <b>ldap_get_next_page</b> until either another page of results are successfully retrieved, an error code is returned, or <b>LDAP_NO_RESULTS_RETURNED</b> is returned to indicate that the search is complete.

If you prefer to retrieve paged search results synchronously, use 
<a href="https://msdn.microsoft.com/44b1b298-9796-4627-945e-4051c20f3c92">ldap_get_next_page_s</a>.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn938561">Functions</a>



<a href="https://msdn.microsoft.com/844093e1-daba-494d-91b3-67455ff2e456">LDAP</a>



<a href="https://msdn.microsoft.com/822411b7-fc49-4b93-8e54-353350ed5de9">Return Values</a>



<a href="https://msdn.microsoft.com/44b1b298-9796-4627-945e-4051c20f3c92">ldap_get_next_page_s</a>



<a href="https://msdn.microsoft.com/17ad1c7e-c3a1-4f6a-8303-fbbedfc36409">ldap_get_paged_count</a>



<a href="https://msdn.microsoft.com/a4292638-0686-4c2d-8c51-1d5d079d5782">ldap_msgfree</a>



<a href="https://msdn.microsoft.com/e047fccc-a875-4360-be1b-3ac3dea15dd6">ldap_result</a>



<a href="https://msdn.microsoft.com/f88d32e3-ac5f-4934-bf84-4007ffd72ac2">ldap_search_init_page</a>
 

 

