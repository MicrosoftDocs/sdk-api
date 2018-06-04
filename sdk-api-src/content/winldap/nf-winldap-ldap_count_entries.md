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

# ldap_count_entries function


## -description


The <b>ldap_count_entries</b> function counts the number of search entries that a server returned.


## -parameters




### -param ld [in]

The session handle.


### -param res [in]

The search result obtained by a call to one of the synchronous search routines or to 
<a href="https://msdn.microsoft.com/e047fccc-a875-4360-be1b-3ac3dea15dd6">ldap_result</a>.


## -returns



If the function succeeds, it returns the number of entries.

If the function fails, the return value is –1 and the function sets the session error parameters in the LDAP data structure.




## -remarks



The <b>ldap_count_entries</b> function returns the number of entries contained, or remaining in a chain of entries. Call the function with the return value from 
<a href="https://msdn.microsoft.com/1692d091-7963-492d-9998-5680a2a81088">ldap_first_entry</a>, 
<a href="https://msdn.microsoft.com/a0920107-6f99-4d28-a12f-c7f952933472">ldap_next_entry</a>, 
<a href="https://msdn.microsoft.com/b9ee4da3-9309-4e2b-95a9-6e0f1625fc79">ldap_first_reference</a>, 
<a href="https://msdn.microsoft.com/ea67f0e9-5cf7-4755-9bfd-856e26589a8d">ldap_next_reference</a>, or 
<a href="https://msdn.microsoft.com/e047fccc-a875-4360-be1b-3ac3dea15dd6">ldap_result</a>.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn938561">Functions</a>



<a href="https://msdn.microsoft.com/1d216f39-6eb4-4c3d-8f97-92835aac2aca">ldap_count_references</a>



<a href="https://msdn.microsoft.com/3b00eeea-a966-4cf1-b945-2f052cae727a">ldap_count_values</a>



<a href="https://msdn.microsoft.com/1692d091-7963-492d-9998-5680a2a81088">ldap_first_entry</a>



<a href="https://msdn.microsoft.com/b9ee4da3-9309-4e2b-95a9-6e0f1625fc79">ldap_first_reference</a>



<a href="https://msdn.microsoft.com/a0920107-6f99-4d28-a12f-c7f952933472">ldap_next_entry</a>



<a href="https://msdn.microsoft.com/ea67f0e9-5cf7-4755-9bfd-856e26589a8d">ldap_next_reference</a>



<a href="https://msdn.microsoft.com/e047fccc-a875-4360-be1b-3ac3dea15dd6">ldap_result</a>
 

 

