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

# ldap_parse_page_control function


## -description


The <b>ldap_parse_page_control</b> parses the results of a search into pages.


## -parameters




### -param ExternalHandle [in]

The session handle.


### -param ServerControls [in]

An array of controls that includes a page control. The page control contains the cookie and total count fields returned by the server.


### -param TotalCount [out]

A pointer to the total count of entries returned in this page (optional).


### -param Cookie [out]

An opaque cookie, used by the server to determine its location in the result set. Use ber_bvfree to free.


## -returns



If the function succeeds, the return value is <b>LDAP_SUCCESS</b>.

If the function fails, it returns an error code. See 
<a href="https://msdn.microsoft.com/822411b7-fc49-4b93-8e54-353350ed5de9">Return Values</a> for more information.




## -remarks



Use <b>ldap_parse_page_control</b> in conjunction with 
<a href="https://msdn.microsoft.com/b3b1f3bd-7eb3-4f76-921c-386562dae2e2">ldap_create_page_control</a> and 
<a href="https://msdn.microsoft.com/6cadfbe0-0b69-4c43-a2ca-d8b3a12bf0a9">ldap_parse_result</a> to implement the simple paging of results by means of controls. After calling <b>ldap_parse_page_control</b> to retrieve the server controls and extract the cookie from the search result, call <b>ldap_parse_result</b> to parse the results. Then use the cookie to call <b>ldap_create_page_control</b> to retrieve the next page of results.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn938561">Functions</a>



<a href="https://msdn.microsoft.com/b3b1f3bd-7eb3-4f76-921c-386562dae2e2">ldap_create_page_control</a>



<a href="https://msdn.microsoft.com/6cadfbe0-0b69-4c43-a2ca-d8b3a12bf0a9">ldap_parse_result</a>
 

 

