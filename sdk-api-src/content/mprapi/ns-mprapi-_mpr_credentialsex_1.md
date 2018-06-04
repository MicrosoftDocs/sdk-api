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

# _MPR_CREDENTIALSEX_1 structure


## -description


The 
<b>MPR_CREDENTIALSEX_1</b> structure contains a pre-shared key used by a demand-dial interface.


## -struct-fields




### -field dwSize

Specifies the size of the data pointed to by the <b>lpbCredentialsInfo</b> member.


### -field lpbCredentialsInfo

Pointer to the pre-shared key.


## -remarks



To a delete a pre-shared key, call 
<a href="https://msdn.microsoft.com/a5372bfb-185c-4562-afa3-35399c8e2a46">MprAdminInterfaceSetCredentials</a> with the <b>MPR_CREDENTIALSEX_1.dwSize</b> member set to zero.




## -see-also




<a href="https://msdn.microsoft.com/0ef9f437-a15b-4f6c-ac76-4c31a23e8792">MprAdminInterfaceGetCredentialsEx</a>



<a href="https://msdn.microsoft.com/d0807c03-3994-4624-97ea-94b55e7cd1e4">MprAdminInterfaceSetCredentialsEx</a>
 

 

