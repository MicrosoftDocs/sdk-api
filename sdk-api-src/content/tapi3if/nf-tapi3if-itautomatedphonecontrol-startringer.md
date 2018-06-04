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

# ITAutomatedPhoneControl::StartRinger


## -description


The 
<b>StartRinger</b> method starts the phone's ringer, specifying the ring mode and the duration of the ring.


## -parameters




### -param lRingMode [in]

Ring mode. The exact meaning of this value is device-dependent. For more information, see the following Remarks section.


### -param lDuration [in]

Length of ring.


## -returns



If the method succeeds, it returns S_OK. Otherwise, it returns an error value.




## -remarks



If you specify the value zero in the <i>lRingMode</i> parameter, and the phone doesn't have a ringer device, the 
<b>StartRinger</b> method attempts to play the ringing sound on the system's default audio render device. Examples of default devices include sound card speakers and a USB phone's audio render device. For more information, see 
<a href="https://msdn.microsoft.com/7a73d5ff-d08a-46e6-b4ad-4f3b973967a7">PHONECAPS_LONG</a>.




## -see-also




<a href="https://msdn.microsoft.com/60d4f079-75ee-4aeb-9e7c-0b16d90da754">ITAutomatedPhoneControl</a>
 

 

