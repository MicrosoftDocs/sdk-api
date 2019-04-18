---
UID: NF:segment.IMSVidAnalogTuner.get_SAP
title: IMSVidAnalogTuner::get_SAP (segment.h)
author: windows-sdk-content
description: The get_SAP method retrieves the tuner's SAP setting to enable secondary audio components.
old-location: mstv\imsvidanalogtuner_get_sap.htm
tech.root: mstv
ms.assetid: 9943ca7e-754e-4145-8f52-0a915fd7133d
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IMSVidAnalogTuner interface [Microsoft TV Technologies],get_SAP method, IMSVidAnalogTuner.get_SAP, IMSVidAnalogTuner::get_SAP, IMSVidAnalogTunerget_SAP, get_SAP, get_SAP method [Microsoft TV Technologies], get_SAP method [Microsoft TV Technologies],IMSVidAnalogTuner interface, mstv.imsvidanalogtuner_get_sap, segment/IMSVidAnalogTuner::get_SAP
ms.topic: method
req.header: segment.h
req.include-header: Msvidctl.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: None supported
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
 - IMSVidAnalogTuner.get_SAP
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMSVidAnalogTuner::get_SAP


## -description


The <b>get_SAP</b> method retrieves the tuner's SAP setting to enable secondary audio components.

This method is currently not supported.


## -parameters




### -param pfSapOn [out]

Pointer to a flag indicating whether SAP is on.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd375962(v=VS.85).aspx">IAMTVAudio Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd694420(v=VS.85).aspx">IMSVidAnalogTuner Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd694434(v=VS.85).aspx">IMSVidAnalogTuner::put_SAP</a>
 

 

