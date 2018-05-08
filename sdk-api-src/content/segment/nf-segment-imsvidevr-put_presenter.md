---
UID: NF:segment.IMSVidEVR.put_Presenter
title: IMSVidEVR::put_Presenter
author: windows-driver-content
description: The put_Presenter method sets the presenter object for the Enhanced Video Renderer (EVR) filter.
old-location: mstv\imsvidevr_put_presenter.htm
old-project: mstv
ms.assetid: 602d92fc-e948-4cea-9bbf-8968c5e31257
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: IMSVidEVR interface [Microsoft TV Technologies],put_Presenter method, IMSVidEVR.put_Presenter, IMSVidEVR::put_Presenter, IMSVidEVRput_Presenter, mstv.imsvidevr_put_presenter, put_Presenter, put_Presenter method [Microsoft TV Technologies], put_Presenter method [Microsoft TV Technologies],IMSVidEVR interface, segment/IMSVidEVR::put_Presenter
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: segment.h
req.include-header: Msvidctl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
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
-	IMSVidEVR.put_Presenter
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IMSVidEVR::put_Presenter


## -description


The <b>put_Presenter</b> method sets the presenter object for the <a href="https://msdn.microsoft.com/ead99cb3-2be2-42c6-ac22-be0c2ddf28d5">Enhanced Video Renderer</a> (EVR) filter.


## -parameters




### -param pAllocPresent [in]

Pointer to a presenter's <a href="https://msdn.microsoft.com/8f6e3132-03e9-4a2e-9160-e39d29cf2408">IMFVideoPresenter</a> interface. This interface is documented in this Media Foundation SDK documentaion.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -see-also




<a href="https://msdn.microsoft.com/437f515b-0353-4ff2-b8c2-5dd27d4e12f7">IMSVidEVR</a>
 

 

