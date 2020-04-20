---
UID: NS:winuser.tagTouchPredictionParameters
title: TOUCHPREDICTIONPARAMETERS (winuser.h)
description: Contains hardware input details that can be used to predict touch targets and help compensate for hardware latency when processing touch and gesture input that contains distance and velocity data.helpviewer_keywords: ["*PTOUCHPREDICTIONPARAMETERS","PTouchPredictionParameters","PTouchPredictionParameters structure pointer [Input Messages and Notifications]","TOUCHPREDICTIONPARAMETERS","TouchPredictionParameters","TouchPredictionParameters structure [Input Messages and Notifications]","_TouchPredictionParameters","inputmsg.touchpredictionparameters_struct","winuser/PTouchPredictionParameters","winuser/TouchPredictionParameters"]
old-location: inputmsg\touchpredictionparameters_struct.htm
tech.root: InputMsg
ms.assetid: 4F7F2B51-B65E-4699-A0FF-55A9A3AF4B61
ms.date: 12/05/2018
ms.keywords: '*PTOUCHPREDICTIONPARAMETERS, PTouchPredictionParameters, PTouchPredictionParameters structure pointer [Input Messages and Notifications], TOUCHPREDICTIONPARAMETERS, TouchPredictionParameters, TouchPredictionParameters structure [Input Messages and Notifications], _TouchPredictionParameters, inputmsg.touchpredictionparameters_struct, winuser/PTouchPredictionParameters, winuser/TouchPredictionParameters'
f1_keywords:
- winuser/TouchPredictionParameters
dev_langs:
- c++
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
targetos: Windows
req.typenames: TOUCHPREDICTIONPARAMETERS, *PTOUCHPREDICTIONPARAMETERS
req.redist: 
ms.custom: 19H1
---

# TOUCHPREDICTIONPARAMETERS structure


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



By default, touch prediction is activated. For information on getting pointer data without deactivating touch prediction, see <a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-getunpredictedmessagepos">GetUnpredictedMessagePos</a>.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/inputmsg/structures">Structures</a>
 

 

