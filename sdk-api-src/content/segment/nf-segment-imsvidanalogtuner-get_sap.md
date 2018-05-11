---
UID: NF:segment.IMSVidAnalogTuner.get_SAP
title: IMSVidAnalogTuner::get_SAP
author: windows-driver-content
description: The get_SAP method retrieves the tuner's SAP setting to enable secondary audio components.
old-location: mstv\imsvidanalogtuner_get_sap.htm
old-project: mstv
ms.assetid: 9943ca7e-754e-4145-8f52-0a915fd7133d
ms.author: windowsdriverdev
ms.date: 5/8/2018
ms.keywords: IMSVidAnalogTuner interface [Microsoft TV Technologies],get_SAP method, IMSVidAnalogTuner.get_SAP, IMSVidAnalogTuner::get_SAP, IMSVidAnalogTunerget_SAP, get_SAP, get_SAP method [Microsoft TV Technologies], get_SAP method [Microsoft TV Technologies],IMSVidAnalogTuner interface, mstv.imsvidanalogtuner_get_sap, segment/IMSVidAnalogTuner::get_SAP
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: SourceSizeList
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	segment.h
api_name:
-	IMSVidAnalogTuner.get_SAP
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
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




<a href="https://msdn.microsoft.com/de340594-4410-4896-b206-0f47d4035bc1">IAMTVAudio Interface</a>



<a href="https://msdn.microsoft.com/640143d3-6712-4e92-a1d9-0689637b3d90">IMSVidAnalogTuner Interface</a>



<a href="https://msdn.microsoft.com/e27efb36-de0c-4255-a5d8-6357f283cd12">IMSVidAnalogTuner::put_SAP</a>
 

 

