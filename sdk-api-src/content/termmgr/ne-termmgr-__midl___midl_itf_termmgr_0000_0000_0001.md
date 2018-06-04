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

# __MIDL___MIDL_itf_termmgr_0000_0000_0001 enumeration


## -description


The 
<b>TMGR_DIRECTION</b> enum is used by the pluggable terminal methods to indicate terminal direction.


## -enum-fields




### -field TMGR_TD_CAPTURE

The terminal can originate a media stream.


### -field TMGR_TD_RENDER

The terminal can render a media stream.


### -field TMGR_TD_BOTH

The terminal can handle both directions of a media stream.


## -see-also




<a href="https://msdn.microsoft.com/67f2f241-2389-476f-a412-af456c1c3376">ITPluggableTerminalClassRegistration::get_Direction</a>



<a href="https://msdn.microsoft.com/b68c0697-e889-471d-857a-d11e974c6552">ITPluggableTerminalClassRegistration::put_Direction</a>
 

 

