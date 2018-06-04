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

# D3D12_PREDICATION_OP enumeration


## -description



          Specifies the predication operation to apply.
        


## -enum-fields




### -field D3D12_PREDICATION_OP_EQUAL_ZERO


            Enables predication if all 64-bits are zero.
          


### -field D3D12_PREDICATION_OP_NOT_EQUAL_ZERO


            Enables predication if at least one of the 64-bits are not zero.
          


## -remarks




          This enum is used by <a href="https://msdn.microsoft.com/21526012-A675-40E8-A11C-4CBA5C12B9CF">SetPredication</a>.
        


          Predication is decoupled from queries.
          Predication can be set based on the value of 64-bits within a buffer.
        




## -see-also




<a href="https://msdn.microsoft.com/76E76C85-128E-4F0E-9711-C72C4CF6C835">Core Enumerations</a>



<a href="https://msdn.microsoft.com/5C5138C7-F6E8-4646-961A-0E2312B5356B">Predication</a>
 

 

