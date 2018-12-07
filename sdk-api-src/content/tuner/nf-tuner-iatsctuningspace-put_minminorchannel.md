---
UID: NF:tuner.IATSCTuningSpace.put_MinMinorChannel
title: IATSCTuningSpace::put_MinMinorChannel
author: windows-sdk-content
description: The put_MinMinorChannel method sets the lowest minor channel number ever allowed for this tuning space.
old-location: mstv\iatsctuningspace_put_minminorchannel.htm
tech.root: mstv
ms.assetid: 71ae8be2-8e80-49ff-9d1b-be42a620c20c
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IATSCTuningSpace interface [Microsoft TV Technologies],put_MinMinorChannel method, IATSCTuningSpace.put_MinMinorChannel, IATSCTuningSpace::put_MinMinorChannel, IATSCTuningSpaceput_MinMinorChannel, mstv.iatsctuningspace_put_minminorchannel, put_MinMinorChannel, put_MinMinorChannel method [Microsoft TV Technologies], put_MinMinorChannel method [Microsoft TV Technologies],IATSCTuningSpace interface, tuner/IATSCTuningSpace::put_MinMinorChannel
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - tuner.h
api_name:
 - IATSCTuningSpace.put_MinMinorChannel
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IATSCTuningSpace::put_MinMinorChannel


## -description



The <b>put_MinMinorChannel</b> method sets the lowest minor channel number ever allowed for this tuning space.




## -parameters




### -param NewMinMinorChannelVal [in]

Variable of type <b>long</b> that specifies the lowest minor channel.


## -returns



Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.




## -remarks



This property must be set after calling <a href="https://msdn.microsoft.com/e90b78da-abd5-40bc-8d88-8a257acabe23">put_MaxMinorChannel</a> to avoid the case where the minimum minor channel is greater than the maximum minor channel. Both properties default to -1 (not set).




## -see-also




<a href="https://msdn.microsoft.com/313508e5-a9b2-42b8-bb2f-d191944d0939">IATSCTuningSpace Interface</a>
 

 

