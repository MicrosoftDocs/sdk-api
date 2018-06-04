---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
 

 

