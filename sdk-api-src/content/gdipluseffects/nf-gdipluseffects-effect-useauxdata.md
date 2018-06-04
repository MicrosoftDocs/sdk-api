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

# Effect::UseAuxData


## -description


The <b>Effect::UseAuxData</b> method sets or clears a flag that specifies whether the <a href="https://msdn.microsoft.com/6b3d0a2f-acff-47a7-bc9f-6e9d659f683c">Bitmap::ApplyEffect</a> method should return a pointer to the auxiliary data that it creates. 


## -parameters




### -param useAuxDataFlag [in]

Type: <b>const BOOL</b>

Set to <b>TRUE</b> to specify that <a href="https://msdn.microsoft.com/6b3d0a2f-acff-47a7-bc9f-6e9d659f683c">ApplyEffect</a> should return a pointer to its auxiliary data; <b>FALSE</b> otherwise.


## -returns



This method does not return a value.




## -see-also




<a href="https://msdn.microsoft.com/7b32aad2-ba44-46a6-8315-d55fed2d9391">Effect</a>



<a href="https://msdn.microsoft.com/b418496f-4304-4885-bcba-c8178b90a788">Effect::GetAuxData</a>



<a href="https://msdn.microsoft.com/c19c3891-2894-4655-b5c8-1306bfb72244">Effect::GetAuxDataSize</a>
 

 

