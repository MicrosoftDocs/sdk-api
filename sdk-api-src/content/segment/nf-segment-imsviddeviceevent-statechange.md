---
UID: NF:segment.IMSVidDeviceEvent.StateChange
title: IMSVidDeviceEvent::StateChange
author: windows-sdk-content
description: This topic applies to Windows XP or later.
old-location: mstv\imsviddeviceevent_statechange.htm
tech.root: MSTV
ms.assetid: 0f7a5e37-5a0d-415e-aca0-df5f9448b017
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IMSVidDeviceEvent interface [Microsoft TV Technologies],StateChange method, IMSVidDeviceEvent.StateChange, IMSVidDeviceEvent::StateChange, IMSVidDeviceEventStateChange, StateChange, StateChange method [Microsoft TV Technologies], StateChange method [Microsoft TV Technologies],IMSVidDeviceEvent interface, mstv.imsviddeviceevent_statechange, segment/IMSVidDeviceEvent::StateChange
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: segment.h
req.include-header: Msvidctl.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Segment.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - segment.h
api_name:
 - IMSVidDeviceEvent.StateChange
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- segment.h
: 
- IMSVidDeviceEvent.StateChange
: 
---

# IMSVidDeviceEvent::StateChange


## -description



This topic applies to Windows XP or later.
        



The <b>StateChange</b> method signals that the state of the device has changed.


## -parameters




### -param lpd

TBD


### -param oldState [in]

Specifies the old state as an <a href="https://msdn.microsoft.com/b4da9c6e-3235-4c78-b9e1-57c9d06fccbc">MSVidCtlStateList</a> value.


### -param newState [in]

Specifies the new state as an <a href="https://msdn.microsoft.com/b4da9c6e-3235-4c78-b9e1-57c9d06fccbc">MSVidCtlStateList</a> value.


#### - plpd [in]

Pointer to the device object that signaled the change.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -remarks



The dispatch identifier (dispid) of this method is <b>eventidStateChange</b>.




## -see-also




<a href="https://msdn.microsoft.com/1a5a9bc1-7d18-4aa9-bc5f-318f7bedbc48">IMSVidDeviceEvent</a>
 

 

