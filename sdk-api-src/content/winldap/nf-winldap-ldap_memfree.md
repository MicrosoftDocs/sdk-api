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

# ldap_memfree function


## -description


The <b>ldap_memfree</b> function frees memory allocated from the LDAP heap.


## -parameters




### -param Block [in]

A pointer to a null-terminated string that contains a pointer to memory allocated by the LDAP library.


## -returns



None.




## -remarks



Call <b>ldap_memfree</b> to free strings, such as the attribute names returned by <b>ldap_*_attribute</b>, or distinguished names returned by 
<a href="https://msdn.microsoft.com/00484fe7-65d2-4300-ab5c-0a69a25e65e6">ldap_get_dn</a>. Do not free the static buffers used by 
<a href="https://msdn.microsoft.com/ebd7303d-e98d-454d-9964-d774d5c2a756">ldap_open</a>, 
<a href="https://msdn.microsoft.com/a633afa1-4a37-4894-ae94-5225d99077fd">ldap_get_values</a>, and others.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn938561">Functions</a>



<a href="https://msdn.microsoft.com/00484fe7-65d2-4300-ab5c-0a69a25e65e6">ldap_get_dn</a>



<a href="https://msdn.microsoft.com/a633afa1-4a37-4894-ae94-5225d99077fd">ldap_get_values</a>



<a href="https://msdn.microsoft.com/ebd7303d-e98d-454d-9964-d774d5c2a756">ldap_open</a>
 

 

