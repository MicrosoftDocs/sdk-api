---
UID: NS:winuser.tagTouchPredictionParameters
title: tagTouchPredictionParameters
author: windows-sdk-content
description: Contains hardware input details that can be used to predict touch targets and help compensate for hardware latency when processing touch and gesture input that contains distance and velocity data.
old-location: inputmsg\touchpredictionparameters_struct.htm
tech.root: InputMsg
ms.assetid: 4F7F2B51-B65E-4699-A0FF-55A9A3AF4B61
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PTOUCHPREDICTIONPARAMETERS, PTouchPredictionParameters, PTouchPredictionParameters structure pointer [Input Messages and Notifications], TOUCHPREDICTIONPARAMETERS, TouchPredictionParameters, TouchPredictionParameters structure [Input Messages and Notifications], _TouchPredictionParameters, inputmsg.touchpredictionparameters_struct, tagTouchPredictionParameters, winuser/PTouchPredictionParameters, winuser/TouchPredictionParameters"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - HeaderDef
api_location:
 - Winuser.h
api_name:
 - TouchPredictionParameters
product: Windows
targetos: Windows
req.typenames: TOUCHPREDICTIONPARAMETERS, *PTOUCHPREDICTIONPARAMETERS
req.redist: 
---

# tagTouchPredictionParameters structure


## -description


Contains hardware input details that can be used to predict touch targets and help compensate for hardware latency when processing touch and gesture input that contains distance and velocity data.


## -struct-fields




### -field cbSize

The size of this structure, in bytes. 


### -field dwLatency

Latency in milliseconds.


### -field dwSampleTime

Sample time in milliseconds (used to calculate velocity).


### -field bUseHWTimeStamp

Use timestamps provided by the hardware.


## -remarks



By default, touch prediction is activated. For information on getting pointer data without deactivating touch prediction, see <a href="https://msdn.microsoft.com/5BE2748B-0124-4647-A77E-EA2937C7B1AD">GetUnpredictedMessagePos</a>.




## -see-also




<a href="https://msdn.microsoft.com/2224DCD0-DAE1-4AC2-AB36-23D114801138">Structures</a>
 

 

