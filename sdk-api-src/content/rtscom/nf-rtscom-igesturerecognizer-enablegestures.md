---
UID: NF:rtscom.IGestureRecognizer.EnableGestures
title: IGestureRecognizer::EnableGestures
author: windows-driver-content
description: Sets a value that indicates to which application gestures the GestureRecognizer Class object responds.
old-location: tablet\igesturerecognizer_enablegestures.htm
old-project: tablet
ms.assetid: 59d39c2c-1c92-4325-b534-36b97a7df20f
ms.author: windowsdriverdev
ms.date: 5/7/2018
ms.keywords: 59d39c2c-1c92-4325-b534-36b97a7df20f, EnableGestures, EnableGestures method [Tablet PC], EnableGestures method [Tablet PC],IGestureRecognizer interface, IGestureRecognizer interface [Tablet PC],EnableGestures method, IGestureRecognizer.EnableGestures, IGestureRecognizer::EnableGestures, rtscom/IGestureRecognizer::EnableGestures, tablet.igesturerecognizer_enablegestures
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: rtscom.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP Tablet PC Edition [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: StylusQueue
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	RTSCom.dll
api_name:
-	IGestureRecognizer.EnableGestures
product: Windows
targetos: Windows
req.lib: 
req.dll: RTSCom.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IGestureRecognizer::EnableGestures


## -description



Sets a value that indicates to which application gestures the <a href="https://msdn.microsoft.com/7cdaf3bf-7aae-4d36-af1c-0eb5a726f388">GestureRecognizer Class</a> object responds.




## -parameters




### -param cGestures [in]

 The size of the array to which the <i>pGestures</i> parameter points. Valid values are between 0 and 64, inclusive.


### -param pGestures [in]

An array of the <a href="https://msdn.microsoft.com/b429ec96-691f-4761-92bf-ef500cf0e1be">InkApplicationGesture Enumeration</a> values that indicates to which application gestures the <a href="https://msdn.microsoft.com/7cdaf3bf-7aae-4d36-af1c-0eb5a726f388">GestureRecognizer Class</a> object responds.


## -returns



For a description of return values, see <a href="https://msdn.microsoft.com/fc0900b4-f08b-4a93-bbc0-d3db067d7917">RealTimeStylus Classes and Interfaces</a>.




## -remarks



You cannot enable <b>AllGestures</b> in conjunction with any other gestures.




## -see-also




<a href="https://msdn.microsoft.com/938e1eb2-3dd4-4e21-9c46-9ef840172b05">DynamicRenderer Class</a>



<a href="https://msdn.microsoft.com/7cdaf3bf-7aae-4d36-af1c-0eb5a726f388">GestureRecognizer Class</a>



<a href="https://msdn.microsoft.com/dfdc00d6-c843-4298-9773-92775406fbf7">IGestureRecognizer</a>



<a href="https://msdn.microsoft.com/4e977348-30d8-474c-80af-56371be5aee4">IGestureRecognizer::Enabled Property</a>
 

 

