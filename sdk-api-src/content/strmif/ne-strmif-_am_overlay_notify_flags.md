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

# _AM_OVERLAY_NOTIFY_FLAGS enumeration


## -description



The AM_OVERLAY_NOTIFY_FLAGS enumeration indicates what the overlay has changed, or is about to change.




## -enum-fields




### -field AM_OVERLAY_NOTIFY_VISIBLE_CHANGE

The rectangle will be changed from visible to invisible, or vice-versa.


### -field AM_OVERLAY_NOTIFY_SOURCE_CHANGE

Source rectangle changed or changing.


### -field AM_OVERLAY_NOTIFY_DEST_CHANGE

Destination rectangle changed or changing.


## -remarks



The <a href="https://msdn.microsoft.com/ede823ba-8340-4339-8e8a-e1d4f9ad1273">IDDrawExclModeVideoCallback::OnUpdateOverlay</a> method uses these flags to indicate how the overlay has changed, so that applications can take the necessary steps.




## -see-also




<a href="https://msdn.microsoft.com/74467006-b077-49c0-8573-f939ac3d3444">DirectShow Enumerated Types</a>



<a href="https://msdn.microsoft.com/ede823ba-8340-4339-8e8a-e1d4f9ad1273">IDDrawExclModeVideoCallback::OnUpdateOverlay</a>
 

 

