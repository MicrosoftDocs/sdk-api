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

# IFEDictionary::GetPosTable


## -description


Obtains the public POS (Part of Speech) table.


## -parameters




### -param prgPosTbl [out]

Pointer to the array of <a href="https://msdn.microsoft.com/CA6A4E71-651A-44CA-B47D-79888A36BB12">POSTBL</a> structures.


### -param pcPosTbl [out]

Pointer to the number of <a href="https://msdn.microsoft.com/CA6A4E71-651A-44CA-B47D-79888A36BB12">POSTBL</a> structures in the returned array. Can be <b>NULL</b>.


## -returns



<b>S_OK</b> if successful, otherwise <b>E_FAIL</b>.




## -see-also




<a href="https://msdn.microsoft.com/4C63FF43-0170-4038-AB01-72441E1BB189">IFEDictionary</a>



<a href="https://msdn.microsoft.com/CA6A4E71-651A-44CA-B47D-79888A36BB12">POSTBL</a>
 

 

