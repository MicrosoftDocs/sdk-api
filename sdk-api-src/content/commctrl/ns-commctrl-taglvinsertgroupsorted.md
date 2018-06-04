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

# tagLVINSERTGROUPSORTED structure


## -description


Used to sort groups. It is used with <a href="https://msdn.microsoft.com/8ad1660b-8b64-4f02-ac1b-b7edeeea38ab">LVM_INSERTGROUPSORTED</a>.


## -struct-fields




### -field pfnGroupCompare

Type: <b>PFNLVGROUPCOMPARE</b>

Pointer to application-defined function <a href="https://msdn.microsoft.com/18e93f11-d215-4c16-b873-5c7b1e725886">LVGroupCompare</a> that is used to sort the groups.


### -field pvData

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPVOID</a>*</b>

Data to sort; this is application-defined.


### -field lvGroup

Type: <b><a href="https://msdn.microsoft.com/512a8524-d5f9-47c0-a28e-47c3c1a713bf">LVGROUP</a></b>

Group to sort; this is application-defined.


## -see-also




<a href="https://msdn.microsoft.com/18e93f11-d215-4c16-b873-5c7b1e725886">LVGroupCompare</a>



<a href="https://msdn.microsoft.com/8ad1660b-8b64-4f02-ac1b-b7edeeea38ab">LVM_INSERTGROUPSORTED</a>



<b>Reference</b>
 

 

