---
UID: NF:tuner.IATSCTuningSpace.get_MaxMinorChannel
title: IATSCTuningSpace::get_MaxMinorChannel
author: windows-driver-content
description: The get_MaxMinorChannel method gets the highest minor channel number for this tuning space.
old-location: mstv\iatsctuningspace_get_maxminorchannel.htm
old-project: mstv
ms.assetid: 55bfef31-f9c2-4edb-b4a9-369424584316
ms.author: windowsdriverdev
ms.date: 5/8/2018
ms.keywords: IATSCTuningSpace interface [Microsoft TV Technologies],get_MaxMinorChannel method, IATSCTuningSpace.get_MaxMinorChannel, IATSCTuningSpace::get_MaxMinorChannel, IATSCTuningSpaceget_MaxMinorChannel, get_MaxMinorChannel, get_MaxMinorChannel method [Microsoft TV Technologies], get_MaxMinorChannel method [Microsoft TV Technologies],IATSCTuningSpace interface, mstv.iatsctuningspace_get_maxminorchannel, tuner/IATSCTuningSpace::get_MaxMinorChannel
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: BITMAP_RENDERER_STATISTICS, *PBITMAP_RENDERER_STATISTICS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	tuner.h
api_name:
-	IATSCTuningSpace.get_MaxMinorChannel
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IATSCTuningSpace::get_MaxMinorChannel


## -description



The <b>get_MaxMinorChannel</b> method gets the highest minor channel number for this tuning space.




## -parameters




### -param MaxMinorChannelVal






#### - pMaxMinorChannelVal [out]

Receives the highest minor channel.


## -returns



Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.




## -see-also




<a href="https://msdn.microsoft.com/313508e5-a9b2-42b8-bb2f-d191944d0939">IATSCTuningSpace Interface</a>
 

 

