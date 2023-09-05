---
UID: NF:segment.IMSVidInputDevice.View
title: IMSVidInputDevice::View (segment.h)
description: The View method configures this input device to view the specified tune request.
helpviewer_keywords: ["IMSVidInputDevice interface [Microsoft TV Technologies]","View method","IMSVidInputDevice.View","IMSVidInputDevice::View","IMSVidInputDeviceView","View","View method [Microsoft TV Technologies]","View method [Microsoft TV Technologies]","IMSVidInputDevice interface","mstv.imsvidinputdevice_view","segment/IMSVidInputDevice::View"]
old-location: mstv\imsvidinputdevice_view.htm
tech.root: mstv
ms.assetid: f106e520-86e5-4b7e-8e16-1f82797f128f
ms.date: 12/05/2018
ms.keywords: IMSVidInputDevice interface [Microsoft TV Technologies],View method, IMSVidInputDevice.View, IMSVidInputDevice::View, IMSVidInputDeviceView, View, View method [Microsoft TV Technologies], View method [Microsoft TV Technologies],IMSVidInputDevice interface, mstv.imsvidinputdevice_view, segment/IMSVidInputDevice::View
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMSVidInputDevice::View
 - segment/IMSVidInputDevice::View
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - segment.h
api_name:
 - IMSVidInputDevice.View
---

# IMSVidInputDevice::View


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>View</b> method configures this input device to view the specified tune request.

## -parameters

### -param v [in]

Specifies the tune request as a <b>VARIANT</b> type.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an error code.

## -remarks

Before calling this method, set the device as the active input by calling the <a href="/previous-versions/windows/desktop/api/msvidctl/nf-msvidctl-imsvidctl-put_inputactive">IMSVidCtl::put_InputActive</a> method. Unless the application needs to choose a specific input device, however, the <a href="/previous-versions/windows/desktop/api/msvidctl/nf-msvidctl-imsvidctl-view">IMSVidCtl::View</a> method is recommended instead of the <b>IMSVidInputDevice::View</b> method.

## -see-also

<a href="/previous-versions/windows/desktop/mstv/msvidinputdevice">IMSVidInputDevice Interface</a>