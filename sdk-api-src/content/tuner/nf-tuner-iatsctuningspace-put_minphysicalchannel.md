---
UID: NF:tuner.IATSCTuningSpace.put_MinPhysicalChannel
title: IATSCTuningSpace::put_MinPhysicalChannel (tuner.h)
description: The put_MinPhysicalChannel method sets the lowest physical channel number for this tuning space.helpviewer_keywords: ["IATSCTuningSpace interface [Microsoft TV Technologies]","put_MinPhysicalChannel method","IATSCTuningSpace.put_MinPhysicalChannel","IATSCTuningSpace::put_MinPhysicalChannel","IATSCTuningSpaceput_MinPhysicalChannel","mstv.iatsctuningspace_put_minphysicalchannel","put_MinPhysicalChannel","put_MinPhysicalChannel method [Microsoft TV Technologies]","put_MinPhysicalChannel method [Microsoft TV Technologies]","IATSCTuningSpace interface","tuner/IATSCTuningSpace::put_MinPhysicalChannel"]
old-location: mstv\iatsctuningspace_put_minphysicalchannel.htm
tech.root: mstv
ms.assetid: 57192470-8013-4812-af95-cb6ce92bea83
ms.date: 12/05/2018
ms.keywords: IATSCTuningSpace interface [Microsoft TV Technologies],put_MinPhysicalChannel method, IATSCTuningSpace.put_MinPhysicalChannel, IATSCTuningSpace::put_MinPhysicalChannel, IATSCTuningSpaceput_MinPhysicalChannel, mstv.iatsctuningspace_put_minphysicalchannel, put_MinPhysicalChannel, put_MinPhysicalChannel method [Microsoft TV Technologies], put_MinPhysicalChannel method [Microsoft TV Technologies],IATSCTuningSpace interface, tuner/IATSCTuningSpace::put_MinPhysicalChannel
f1_keywords:
- tuner/IATSCTuningSpace.put_MinPhysicalChannel
dev_langs:
- c++
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
- IATSCTuningSpace.put_MinPhysicalChannel
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IATSCTuningSpace::put_MinPhysicalChannel


## -description



The <b>put_MinPhysicalChannel</b> method sets the lowest physical channel number for this tuning space.




## -parameters




### -param NewMinPhysicalChannelVal [in]

Variable of type <b>long</b> that specifies the lowest physical channel.


## -returns



Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nn-tuner-iatsctuningspace">IATSCTuningSpace Interface</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-ichanneltunerequest-put_channel">IChannelTuneRequest::put_Channel</a>
 

 

