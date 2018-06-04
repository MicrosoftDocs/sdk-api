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

# IMSVidTunerEvent::TuneChanged


## -description



This topic applies to Windows XP or later.
        



The <b>TuneChanged</b> method signals that the tuner has tuned to a new frequency.


## -parameters




### -param lpd






#### - plpd [in]

Pointer to the <b>MSVidTuner</b> object that fired the event.


## -returns



Return S_OK or an error code.




## -remarks



The dispatch identifier (dispid) of this method is <b>eventidOnTuneChanged</b>.




## -see-also




<a href="https://msdn.microsoft.com/cdffe6ca-00b0-4230-963d-b4409413e5f5">IMSVidTunerEvent Interface</a>
 

 

