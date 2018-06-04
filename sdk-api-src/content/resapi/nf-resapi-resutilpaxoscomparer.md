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

# ResUtilPaxosComparer function


## -description


Compares two Paxos tags and indicates whether they have the same values.


## -parameters




### -param left [in]

The <a href="https://msdn.microsoft.com/732CB125-F43A-4CC4-BC3F-EFB511BB7F2E">PaxosTagCStruct</a> structure that represents the first Paxos tag to use in the comparison.


### -param right [in]

The <a href="https://msdn.microsoft.com/732CB125-F43A-4CC4-BC3F-EFB511BB7F2E">PaxosTagCStruct</a> structure that represents the second  Paxos tag to use in the comparison.


## -returns



<b>TRUE</b> if the Paxos tags have the same values; otherwise <b>FALSE</b>.




## -see-also




<a href="https://msdn.microsoft.com/42eb7c1b-6bd6-4997-b33e-ed16470c8475">Resource Utility Functions</a>
 

 

