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

# ldap_check_filterW function


## -description


The <b>ldap_check_filter</b> function is used to verify filter syntax.


## -parameters




### -param ld [in]

The session handle.


### -param SearchFilter [in]

A pointer to a wide, null-terminated string that contains the name of the filter to check.


## -returns



If the function succeeds, <b>LDAP_SUCCESS</b> is returned.

If the function fails, an error code is returned. For more information, see 
<a href="https://msdn.microsoft.com/822411b7-fc49-4b93-8e54-353350ed5de9">Return Values</a>.




## -remarks



Use <b>ldap_check_filter</b> to verify the syntax of a search filter before initiating a search. This syntax check does not perform a full verification of the search filter syntax against RFC 2254 rules. Rather, it verifies that the filter meets the minimum syntactic requirements for encoding required by the wldap32 search-filter-encoding routines. As a result, a search filter can pass an <b>ldap_check_filter</b> operation, and can be encoded by wldap32, but the server may still detect a RFC 2254 compliance violation and reject the search filter.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn938561">Functions</a>



<a href="https://msdn.microsoft.com/822411b7-fc49-4b93-8e54-353350ed5de9">Return Values</a>



<a href="https://msdn.microsoft.com/fe0d782b-8faf-4666-a952-e2bfd33f6d67">ldap_search</a>
 

 

