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

# D3D12_INFO_QUEUE_FILTER_DESC structure


## -description



          Allow or deny certain types of messages to pass through a filter.


## -struct-fields




### -field NumCategories

Number of message categories to allow or deny.




### -field pCategoryList


            Array of message categories to allow or deny. Array must have at least <i>NumCategories</i> members (see <a href="https://msdn.microsoft.com/297923A3-CE6A-46AF-B8B6-E2AE0C1920CC">D3D12_MESSAGE_CATEGORY</a>).




### -field NumSeverities


            Number of message severity levels to allow or deny.




### -field pSeverityList


            Array of message severity levels to allow or deny. Array must have at least <i>NumSeverities</i> members (see <a href="https://msdn.microsoft.com/44D94C37-4BA8-49FC-BEEF-6666AD59B627">D3D12_MESSAGE_SEVERITY</a>).




### -field NumIDs


            Number of message IDs to allow or deny.


          


### -field pIDList


            Array of message IDs to allow or deny. Array must have at least <i>NumIDs</i> members (see <a href="https://msdn.microsoft.com/95681EB0-C00B-42C8-91E1-1D1F657C886B">D3D12_MESSAGE_ID</a>).


          


## -remarks




          For use with an <a href="https://msdn.microsoft.com/61667AAC-05AC-4745-8992-E9377641D411">ID3D12InfoQueue</a> Interface.




## -see-also




<a href="https://msdn.microsoft.com/FE8796A7-98D1-4333-8755-2A47567560B3">Debug Layer Structures</a>
 

 

