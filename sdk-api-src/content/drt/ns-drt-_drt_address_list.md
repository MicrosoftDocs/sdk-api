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

# _DRT_ADDRESS_LIST structure


## -description


The <b>DRT_ADDRESS_LIST</b> structure contains a set of  <a href="https://msdn.microsoft.com/d6b00d5e-14f1-4e56-b8c8-f3936f6ae9fb">DRT_ADDRESS</a> structures that represent the nodes contacted during a search for a key.


## -struct-fields




### -field AddressCount

The count of entries in <b>AddressList</b>.


### -field AddressList

An array of <a href="https://msdn.microsoft.com/d6b00d5e-14f1-4e56-b8c8-f3936f6ae9fb">DRT_ADDRESS</a> structures that contain information about addresses that participated  in the search operation.


## -see-also




<a href="https://msdn.microsoft.com/d6b00d5e-14f1-4e56-b8c8-f3936f6ae9fb">DRT_ADDRESS</a>



<a href="https://msdn.microsoft.com/b89ea470-072e-46b6-9f5d-3e05aa012188">DrtGetSearchResult</a>
 

 

