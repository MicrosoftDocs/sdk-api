---
UID: NF:segment.IMSVidEVR.get_Presenter
title: IMSVidEVR::get_Presenter
author: windows-sdk-content
description: "."
old-location: mstv\imsvidevr_get_presenter.htm
old-project: mstv
ms.assetid: d3b5e272-8c71-4e84-b08f-b277eec643c4
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: IMSVidEVR interface [Microsoft TV Technologies],get_Presenter method, IMSVidEVR.get_Presenter, IMSVidEVR::get_Presenter, IMSVidEVRget_Presenter, get_Presenter, get_Presenter method [Microsoft TV Technologies], get_Presenter method [Microsoft TV Technologies],IMSVidEVR interface, mstv.imsvidevr_get_presenter, segment/IMSVidEVR::get_Presenter
ms.prod: windows
ms.technology: windows-sdk
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
-	IMSVidEVR.get_Presenter
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IMSVidEVR::get_Presenter


## -description




The <b>get_Presenter</b> method retrieves the presenter object for the <a href="https://msdn.microsoft.com/ead99cb3-2be2-42c6-ac22-be0c2ddf28d5">Enhanced Video Renderer</a> (EVR) filter.


## -parameters




### -param ppAllocPresent [out]

Receives a pointer to the <a href="https://msdn.microsoft.com/8f6e3132-03e9-4a2e-9160-e39d29cf2408">IMFVideoPresenter</a> interface. This interface is documented in this Media Foundation SDK documentaion. The caller must release the interface.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -see-also




<a href="https://msdn.microsoft.com/437f515b-0353-4ff2-b8c2-5dd27d4e12f7">IMSVidEVR</a>
 

 

