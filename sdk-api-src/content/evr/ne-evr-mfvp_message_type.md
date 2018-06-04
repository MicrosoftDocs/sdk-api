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

# MFVP_MESSAGE_TYPE enumeration


## -description


Defines messages for an enhanced video renderer (EVR) presenter. This enumeration is used with the <a href="https://msdn.microsoft.com/f7113cb3-2ea9-4d4f-b6c7-ef4e1025cc6d">IMFVideoPresenter::ProcessMessage</a> method.


## -enum-fields




### -field MFVP_MESSAGE_FLUSH

The presenter should discard any pending samples. The <i>ulParam</i> parameter is not used and should be zero.


### -field MFVP_MESSAGE_INVALIDATEMEDIATYPE

The mixer's output format has changed. The EVR will initiate format negotiation. The <i>ulParam</i> parameter is not used and should be zero.


### -field MFVP_MESSAGE_PROCESSINPUTNOTIFY

One input stream on the mixer has received a new sample. The <i>ulParam</i> parameter is not used and should be zero.


### -field MFVP_MESSAGE_BEGINSTREAMING

The EVR switched from stopped to paused. The presenter should allocate resources. The <i>ulParam</i> parameter is not used and should be zero.


### -field MFVP_MESSAGE_ENDSTREAMING

The EVR switched from running or paused to stopped. The presenter should free resources. The <i>ulParam</i> parameter is not used and should be zero.


### -field MFVP_MESSAGE_ENDOFSTREAM

All streams have ended. The <i>ulParam</i> parameter is not used and should be zero.


### -field MFVP_MESSAGE_STEP

Requests a frame step. The lower <b>DWORD</b> of the <i>ulParam</i> parameter contains the number of frames to step. If the value is <i>N</i>, the presenter should skip <i>N</i>–1 frames and display the <i>N</i> th frame. When that frame has been displayed, the presenter should send an <b>EC_STEP_COMPLETE</b> event to the EVR. If the presenter is not paused when it receives this message, it should return MF_E_INVALIDREQUEST.


### -field MFVP_MESSAGE_CANCELSTEP

Cancels a frame step. The <i>ulParam</i> parameter is not used and should be zero.


## -see-also




<a href="https://msdn.microsoft.com/1c985558-d25d-4f51-978a-58c05943dab9">Enhanced Video Renderer</a>



<a href="https://msdn.microsoft.com/f26a730f-18c4-4247-acaf-af1dfad19086">Media Foundation Enumerations</a>
 

 

