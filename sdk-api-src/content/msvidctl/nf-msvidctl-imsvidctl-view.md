---
UID: NF:msvidctl.IMSVidCtl.View
title: IMSVidCtl::View
author: windows-sdk-content
description: The View method configures the Video Control to view an input source, which can be a tune request, a DVD, or a media file.
old-location: mstv\imsvidctl_view.htm
tech.root: MSTV
ms.assetid: ec0e2a88-13c0-42f3-ba7d-8ebff1234b86
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: IMSVidCtl interface [Microsoft TV Technologies],View method, IMSVidCtl.View, IMSVidCtl::View, IMSVidCtlView, View, View method [Microsoft TV Technologies], View method [Microsoft TV Technologies],IMSVidCtl interface, mstv.imsvidctl_view, msvidctl/IMSVidCtl::View
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: msvidctl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Msvidctl.idl
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
 - msvidctl.h
api_name:
 - IMSVidCtl.View
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMSVidCtl::View


## -description


The <b>View</b> method configures the Video Control to view an input source, which can be a tune request, a DVD, or a media file.


## -parameters




### -param v

TBD




#### - pv [in]

Pointer to the input source as a <b>VARIANT</b> type. This parameter must be one of the following:<ul>
<li>A pointer to a valid tune request object that supports the <a href="https://msdn.microsoft.com/34077b45-32b4-466b-b103-6a42fc869265">ITuneRequest</a> interface. The tune request must be initialized with all the tuning information required for the particular network type.</li>
<li>The string "DVD:" for DVD playback.</li>
<li>The name of a media file.</li>
</ul>



## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -remarks



If the Video Control already has an active input device, this method configures the device for the specified input. Otherwise, this method locates an input device that can handle the input and activates it.

An input device typically corresponds to a source filter. If the <i>pv</i> parameter is a tune request object, the Video Control determines which filter to use by examining the network type on the tune request. For digital television, the input device will be a BDA Network Provider filter. For analog television, it will be a WDM TV Tuner filter. The specific name and implementation of the filter are device-dependent.

After calling <b>View</b>, use the following methods to build and run the filter graph:

<ul>
<li>The <a href="https://msdn.microsoft.com/49f78dd8-f26e-456d-b67e-155ae0ed5419">IMSVidCtl::Build</a> method builds the rest of the filter graph, based on the selected input and the active features collection. The <b>Build</b> method leaves the graph in a stopped state.</li>
<li>The <a href="https://msdn.microsoft.com/37ed6d7b-2e44-4bce-b476-8e8b28635346">IMSVidCtl::Run</a> method calls <a href="https://msdn.microsoft.com/49f78dd8-f26e-456d-b67e-155ae0ed5419">Build</a> if the graph is not built, and puts the graph into a running state. When the filter graph runs, the video control starts playing the specified tune request.</li>
</ul>
If the filter graph is already built and running, an application can call <b>View</b> to specify a new tune request, either on the same network type or on a different network type.

If the <b>View</b> method succeeds, you can obtain the input device by calling the <a href="https://msdn.microsoft.com/3451002b-5339-4b43-aefd-d66c48f7ae57">IMSVidCtl::get_InputActive</a> method.

You can specify a particular input device by calling the <a href="https://msdn.microsoft.com/696d8ece-a377-4fe8-a790-a68d1a24e65a">IMSVidCtl::put_InputActive</a> method and then calling <a href="https://msdn.microsoft.com/f106e520-86e5-4b7e-8e16-1f82797f128f">IMSVidInputDevice::View</a> on the device, instead of calling <b>View</b> on the Video Control. This might be useful if the local system has multiple devices of the same type. The <b>View</b> method is preferred, however, because it automatically locates the correct device type.


#### Examples

The following example shows how to submit a tune request to the Video Control:


```cpp

ITuneRequest *pTuneReq;
/* Obtain the tune request (not shown). */
CComVariant varTuneRequest = pTuneReq;
hr = pVidControl->View(&varTuneRequest);

```


The following example shows how to play a local file:


```cpp

CComVariant varFileName(OLESTR("C:Example.avi"));
hr = pVidControl->View(&varFileName);

```





## -see-also




<a href="https://msdn.microsoft.com/2330ddf5-4188-4aee-837e-814e83f39cbb">DVD Applications in Visual Basic (Video Control)</a>



<a href="https://msdn.microsoft.com/e3ea10ea-bfb4-4c35-9933-5ad0367fd9ee">IMSVidCtl Interface</a>



<a href="https://msdn.microsoft.com/7ed22c3e-745a-4680-a5fc-accef56ab348">IMSVidCtl::get_InputsAvailable</a>
 

 

