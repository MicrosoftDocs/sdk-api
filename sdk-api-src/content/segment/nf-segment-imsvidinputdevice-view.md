---
UID: NF:segment.IMSVidInputDevice.View
title: IMSVidInputDevice::View
author: windows-sdk-content
description: The View method configures this input device to view the specified tune request.
old-location: mstv\imsvidinputdevice_view.htm
old-project: mstv
ms.assetid: f106e520-86e5-4b7e-8e16-1f82797f128f
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: IMSVidInputDevice interface [Microsoft TV Technologies],View method, IMSVidInputDevice.View, IMSVidInputDevice::View, IMSVidInputDeviceView, View, View method [Microsoft TV Technologies], View method [Microsoft TV Technologies],IMSVidInputDevice interface, mstv.imsvidinputdevice_view, segment/IMSVidInputDevice::View
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: SourceSizeList
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - segment.h
api_name:
 - IMSVidInputDevice.View
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IMSVidInputDevice::View


## -description


The <b>View</b> method configures this input device to view the specified tune request.


## -parameters




### -param v






#### - pv [in]

Specifies the tune request as a <b>VARIANT</b> type.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -remarks



Before calling this method, set the device as the active input by calling the <a href="https://msdn.microsoft.com/696d8ece-a377-4fe8-a790-a68d1a24e65a">IMSVidCtl::put_InputActive</a> method. Unless the application needs to choose a specific input device, however, the <a href="https://msdn.microsoft.com/ec0e2a88-13c0-42f3-ba7d-8ebff1234b86">IMSVidCtl::View</a> method is recommended instead of the <b>IMSVidInputDevice::View</b> method.




## -see-also




<a href="https://msdn.microsoft.com/5b413ade-4ab2-45fa-98b2-fd93c8f89a43">IMSVidInputDevice Interface</a>
 

 

