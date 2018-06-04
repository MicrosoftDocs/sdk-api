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

# ldap_count_references function


## -description


The <b>ldap_count_references</b> function counts the number of subordinate references that were returned by the server in a response to a search request.


## -parameters




### -param ld [in]

The session handle.


### -param res [in]

The search result obtained by a call to one of the synchronous search routines or to 
<a href="https://msdn.microsoft.com/e047fccc-a875-4360-be1b-3ac3dea15dd6">ldap_result</a>.


## -returns



If the function succeeds, it returns the number of references.

If the function fails, it returns –1 and sets the session error parameters in the LDAP data structure.




## -remarks



The <b>ldap_count_references</b> function returns the number of references contained in a chain of search results. It can also be used to count the number of references that remain in a chain. Call the function with the return value from 
<a href="https://msdn.microsoft.com/1692d091-7963-492d-9998-5680a2a81088">ldap_first_entry</a>, 
<a href="https://msdn.microsoft.com/a0920107-6f99-4d28-a12f-c7f952933472">ldap_next_entry</a>, 
<a href="https://msdn.microsoft.com/b9ee4da3-9309-4e2b-95a9-6e0f1625fc79">ldap_first_reference</a>, 
<a href="https://msdn.microsoft.com/ea67f0e9-5cf7-4755-9bfd-856e26589a8d">ldap_next_reference</a>, or 
<a href="https://msdn.microsoft.com/e047fccc-a875-4360-be1b-3ac3dea15dd6">ldap_result</a>.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn938561">Functions</a>



<a href="https://msdn.microsoft.com/6e53b914-2ad8-408a-9671-50a01a8a42f1">ldap_count_entries</a>



<a href="https://msdn.microsoft.com/3b00eeea-a966-4cf1-b945-2f052cae727a">ldap_count_values</a>



<a href="https://msdn.microsoft.com/1692d091-7963-492d-9998-5680a2a81088">ldap_first_entry</a>



<a href="https://msdn.microsoft.com/b9ee4da3-9309-4e2b-95a9-6e0f1625fc79">ldap_first_reference</a>



<a href="https://msdn.microsoft.com/a0920107-6f99-4d28-a12f-c7f952933472">ldap_next_entry</a>



<a href="https://msdn.microsoft.com/ea67f0e9-5cf7-4755-9bfd-856e26589a8d">ldap_next_reference</a>



<a href="https://msdn.microsoft.com/e047fccc-a875-4360-be1b-3ac3dea15dd6">ldap_result</a>
 

 

