---
UID: NF:winldap.ldap_get_paged_count
title: ldap_get_paged_count function
author: windows-sdk-content
description: Records the number of paged results that the server has returned for a search.
old-location: ldap\ldap_get_paged_count.htm
old-project: ldap
ms.assetid: 17ad1c7e-c3a1-4f6a-8303-fbbedfc36409
ms.author: windowssdkdev
ms.date: 06/14/2018
ms.keywords: "_ldap_ldap_get_paged_count, ldap.ldap__get__paged__count, ldap.ldap_get_paged_count, ldap_get_paged_count, ldap_get_paged_count function [LDAP], winldap/ldap_get_paged_count"
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
tech.root: 
req.typenames: VOLUME_GET_GPT_ATTRIBUTES_INFORMATION, *PVOLUME_GET_GPT_ATTRIBUTES_INFORMATION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wldap32.dll
api_name:
 - ldap_get_paged_count
product: Windows
targetos: Windows
req.lib: Wldap32.lib
req.dll: Wldap32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# ldap_get_paged_count function


## -description


The <b>ldap_get_paged_count</b> function records the number of paged results that the server has returned for a search.


## -parameters




### -param ExternalHandle [in]

The session handle.


### -param SearchBlock [in]

Handle to an 
<a href="https://msdn.microsoft.com/70bdbb05-ac7f-48af-9241-e2a70b6b16ab">LDAPSearch</a> structure.


### -param TotalCount [out]

The total pages in the search results.


### -param Results [out]

A pointer to the 
<a href="https://msdn.microsoft.com/547a0736-23a4-4bfd-8ae0-866825228b53">LDAPMessage</a> structure that contains the results of the operation.


## -returns



If the function succeeds, the return value is <b>LDAP_SUCCESS</b>.

If the function fails, it returns an error code. For more information, see 
<a href="https://msdn.microsoft.com/822411b7-fc49-4b93-8e54-353350ed5de9">Return Values</a>.




## -remarks



Call <b>ldap_get_paged_count</b> for each  result set received after calling 
<a href="https://msdn.microsoft.com/34ddf4d4-3a89-42e0-850d-fcc1c942cb3b">ldap_get_next_page</a>. This allows the LDAP runtime to save from the cookie that the server uses to track  the search.

If you call 
<a href="https://msdn.microsoft.com/44b1b298-9796-4627-945e-4051c20f3c92">ldap_get_next_page_s</a>, a call to <b>ldap_get_paged_count</b> is not required.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn938561">Functions</a>



<a href="https://msdn.microsoft.com/547a0736-23a4-4bfd-8ae0-866825228b53">LDAPMessage</a>



<a href="https://msdn.microsoft.com/70bdbb05-ac7f-48af-9241-e2a70b6b16ab">LDAPSearch</a>



<a href="https://msdn.microsoft.com/822411b7-fc49-4b93-8e54-353350ed5de9">Return Values</a>



<a href="https://msdn.microsoft.com/34ddf4d4-3a89-42e0-850d-fcc1c942cb3b">ldap_get_next_page</a>



<a href="https://msdn.microsoft.com/44b1b298-9796-4627-945e-4051c20f3c92">ldap_get_next_page_s</a>
 

 

