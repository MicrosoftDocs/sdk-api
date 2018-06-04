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

# D3D10_INFO_QUEUE_FILTER structure


## -description


Debug message filter; contains a lists of message types to allow or deny.


## -struct-fields




### -field AllowList

Type: <b><a href="https://msdn.microsoft.com/574cb8e3-4923-4731-b99d-680749fffbae">D3D10_INFO_QUEUE_FILTER_DESC</a></b>

A <a href="https://msdn.microsoft.com/574cb8e3-4923-4731-b99d-680749fffbae">D3D10_INFO_QUEUE_FILTER_DESC</a> structure describing the types of messages the info queue should allow.


### -field DenyList

Type: <b><a href="https://msdn.microsoft.com/574cb8e3-4923-4731-b99d-680749fffbae">D3D10_INFO_QUEUE_FILTER_DESC</a></b>

A <a href="https://msdn.microsoft.com/574cb8e3-4923-4731-b99d-680749fffbae">D3D10_INFO_QUEUE_FILTER_DESC</a> structure describing the types of messages the info queue should reject.


## -remarks



For use with an <a href="https://msdn.microsoft.com/b1405273-53f4-49da-acf5-832e73a25ac2">ID3D10InfoQueue Interface</a>.

Providing an allow list with non-zero values causes only the specified combination of categories, severities and message IDs to be allowed.  
      Messages that do not match the specified combination will be rejected.

Providing a deny list with non-zero values causes the specified combination of categories, severities and message IDs to be rejected.
      Messages that do not match the specified combination will be allowed.




## -see-also




<a href="https://msdn.microsoft.com/84769515-3f3b-4464-9620-7b806bf905b3">Core Structures</a>
 

 

