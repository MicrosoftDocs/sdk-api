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

# DwmRenderGesture function


## -description


Notifies Desktop Window Manager (DWM) that a touch contact has been recognized as a gesture, and that DWM should draw feedback for that gesture.


## -parameters




### -param gt [in]

The type of gesture, specified as one of the <a href="https://msdn.microsoft.com/3FBDDFC9-A3E7-43DC-B7C6-A23976861C28">GESTURE_TYPE</a> values.


### -param cContacts [in]

The number of contact points.


### -param pdwPointerID [in]

The pointer ID.


### -param pPoints [in]

The points.

