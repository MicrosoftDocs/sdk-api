---
UID: NF:msvidctl.IMSVidCtl.View
title: IMSVidCtl::View (msvidctl.h)
description: The View method configures the Video Control to view an input source, which can be a tune request, a DVD, or a media file.
helpviewer_keywords: ["IMSVidCtl interface [Microsoft TV Technologies]","View method","IMSVidCtl.View","IMSVidCtl::View","IMSVidCtlView","View","View method [Microsoft TV Technologies]","View method [Microsoft TV Technologies]","IMSVidCtl interface","mstv.imsvidctl_view","msvidctl/IMSVidCtl::View"]
old-location: mstv\imsvidctl_view.htm
tech.root: mstv
ms.assetid: ec0e2a88-13c0-42f3-ba7d-8ebff1234b86
ms.date: 12/05/2018
ms.keywords: IMSVidCtl interface [Microsoft TV Technologies],View method, IMSVidCtl.View, IMSVidCtl::View, IMSVidCtlView, View, View method [Microsoft TV Technologies], View method [Microsoft TV Technologies],IMSVidCtl interface, mstv.imsvidctl_view, msvidctl/IMSVidCtl::View
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMSVidCtl::View
 - msvidctl/IMSVidCtl::View
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msvidctl.h
api_name:
 - IMSVidCtl.View
---

# IMSVidCtl::View


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>View</b> method configures the Video Control to view an input source, which can be a tune request, a DVD, or a media file.

## -parameters

### -param v [in]

Pointer to the input source as a <b>VARIANT</b> type. This parameter must be one of the following:<ul>
<li>A pointer to a valid tune request object that supports the <a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-itunerequest">ITuneRequest</a> interface. The tune request must be initialized with all the tuning information required for the particular network type.</li>
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
<li>The <a href="/previous-versions/windows/desktop/api/msvidctl/nf-msvidctl-imsvidctl-build">IMSVidCtl::Build</a> method builds the rest of the filter graph, based on the selected input and the active features collection. The <b>Build</b> method leaves the graph in a stopped state.</li>
<li>The <a href="/previous-versions/windows/desktop/api/msvidctl/nf-msvidctl-imsvidctl-run">IMSVidCtl::Run</a> method calls <a href="/previous-versions/windows/desktop/api/msvidctl/nf-msvidctl-imsvidctl-build">Build</a> if the graph is not built, and puts the graph into a running state. When the filter graph runs, the video control starts playing the specified tune request.</li>
</ul>
If the filter graph is already built and running, an application can call <b>View</b> to specify a new tune request, either on the same network type or on a different network type.

If the <b>View</b> method succeeds, you can obtain the input device by calling the <a href="/previous-versions/windows/desktop/api/msvidctl/nf-msvidctl-imsvidctl-get_inputactive">IMSVidCtl::get_InputActive</a> method.

You can specify a particular input device by calling the <a href="/previous-versions/windows/desktop/api/msvidctl/nf-msvidctl-imsvidctl-put_inputactive">IMSVidCtl::put_InputActive</a> method and then calling <a href="/windows/desktop/api/segment/nf-segment-imsvidinputdevice-view">IMSVidInputDevice::View</a> on the device, instead of calling <b>View</b> on the Video Control. This might be useful if the local system has multiple devices of the same type. The <b>View</b> method is preferred, however, because it automatically locates the correct device type.


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

<a href="/previous-versions/windows/desktop/mstv/dvd-applications-in-visual-basic--video-control">DVD Applications in Visual Basic (Video Control)</a>



<a href="/previous-versions/windows/desktop/mstv/msvidctl">IMSVidCtl Interface</a>



<a href="/previous-versions/windows/desktop/api/msvidctl/nf-msvidctl-imsvidctl-get_inputsavailable">IMSVidCtl::get_InputsAvailable</a>