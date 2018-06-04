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

# D3D12_INFO_QUEUE_FILTER structure


## -description



          Debug message filter; contains a lists of message types to allow or deny.


## -struct-fields




### -field AllowList


            Specifies types of messages that you want to allow. See <a href="https://msdn.microsoft.com/079494EC-3FC3-490D-B2BC-0FBD976ECC97">D3D12_INFO_QUEUE_FILTER_DESC</a>.


          


### -field DenyList


            Specifies types of messages that you want to deny.


          


## -remarks




          For use with an <a href="https://msdn.microsoft.com/61667AAC-05AC-4745-8992-E9377641D411">ID3D12InfoQueue</a> Interface.




## -see-also




<a href="https://msdn.microsoft.com/FE8796A7-98D1-4333-8755-2A47567560B3">Debug Layer Structures</a>
 

 

