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

# IInkRecognizer::get_PreferredPacketDescription


## -description



Gets an array of globally unique identifiers (GUIDs) that represents the preferred packet properties for the recognizer.



This property is read-only.


## -parameters


## -remarks



This property describes the contents of a packet and does not allow access to the data that the packet contains.

This property lists the packet properties that the recognizer uses to complete recognition. For all of the Microsoft recognizers, the <b>PreferredPacketDescription</b> property refers to the data describing (x, y) coordinates within an <a href="https://msdn.microsoft.com/b18464ba-feb6-4bb5-9fcf-82feff9bcce4">IInkStrokeDisp</a> object. This data is represented by the X and Y fields of the <a href="https://msdn.microsoft.com/3e8495f6-0860-4ea8-a258-784eaade85c7">packet property</a> constants. A packet contains this point data as well as other data that is related to that stroke, such as the pressure of the pen that made the stroke, the angle of the pen, and so on. The Microsoft recognizers ignore pressure, tilt, and other packet properties.




## -see-also




<a href="https://msdn.microsoft.com/97f982b6-f330-4053-91a9-2a4edc13b4b0">IInkRecognizer Interface</a>



<a href="https://msdn.microsoft.com/3e8495f6-0860-4ea8-a258-784eaade85c7">PacketPropertyGuids Constants</a>
 

 

