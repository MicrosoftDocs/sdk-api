---
UID: NF:tuner.IATSCTuningSpace.get_MinMinorChannel
title: IATSCTuningSpace::get_MinMinorChannel
author: windows-sdk-content
description: The get_MinMinorChannel method gets the lowest minor channel number ever allowed for this tuning space.
old-location: mstv\iatsctuningspace_get_minminorchannel.htm
old-project: mstv
ms.assetid: 93068602-0efa-45f2-9883-d8b681cd3a0f
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: IATSCTuningSpace interface [Microsoft TV Technologies],get_MinMinorChannel method, IATSCTuningSpace.get_MinMinorChannel, IATSCTuningSpace::get_MinMinorChannel, IATSCTuningSpaceget_MinMinorChannel, get_MinMinorChannel, get_MinMinorChannel method [Microsoft TV Technologies], get_MinMinorChannel method [Microsoft TV Technologies],IATSCTuningSpace interface, mstv.iatsctuningspace_get_minminorchannel, tuner/IATSCTuningSpace::get_MinMinorChannel
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: tuner.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Tuner.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: BITMAP_RENDERER_STATISTICS, *PBITMAP_RENDERER_STATISTICS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	tuner.h
api_name:
-	IATSCTuningSpace.get_MinMinorChannel
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IATSCTuningSpace::get_MinMinorChannel


## -description



The <b>get_MinMinorChannel</b> method gets the lowest minor channel number ever allowed for this tuning space.




## -parameters




### -param MinMinorChannelVal






#### - pMinMinorChannelVal [out]

Receives the lowest minor channel.


## -returns



Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.




## -see-also




<a href="https://msdn.microsoft.com/313508e5-a9b2-42b8-bb2f-d191944d0939">IATSCTuningSpace Interface</a>
 

 

