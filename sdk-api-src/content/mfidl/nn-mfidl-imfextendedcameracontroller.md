---
UID: NN:mfidl.IMFExtendedCameraController
title: IMFExtendedCameraController
ms.date: 08/05/2022
targetos: Windows
description: The IMFExtendedCameraController interface allows apps to retrieve an instance of IMFExtendedCameraControl, which is used to configure a capture device's extended properties.
tech.root: mf
req.assembly: 
req.construct-type: iface
req.ddi-compliance: 
req.header: mfidl.h
req.idl: 
req.include-header: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 10 Build 19041
req.target-min-winversvr: Windows 10 Build 19041
req.target-type: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - mfidl.h
api_name:
 - IMFExtendedCameraController
f1_keywords:
 - IMFExtendedCameraController
 - mfidl/IMFExtendedCameraController
dev_langs:
 - c++
---

## -description

Allows apps to retrieve an instance of [IMFExtendedCameraControl](nn-mfidl-imfextendedcameracontrol.md), which is used to configure a capture device's extended properties.

## -remarks

The IMFExtendedCameraController interface can be obtained through the [IMFMediaSource](nn-mfidl-imfmediasource.md) that represents the video capture device and its [IMFGetService](nn-mfidl-imfgetservice.md) implementation.
In this case, guidService parameter of the IMFGetService::GetService function must be `GUID_NULL`, please see following code snippet.

```
HRESULT GetExtendedCameraController(_In_ IMFMediaSource* pCameraSource)
{
    wil::com_ptr_nothrow<IMFExtendedCameraController> spExtCameraController;
    wil::com_ptr_nothrow<IMFGetService> spGetService;

    RETURN_IF_FAILED(pCameraSource->QueryInterface(IID_PPV_ARGS(&spGetService)));
    RETURN_IF_FAILED(spGetService->GetService(GUID_NULL, IID_PPV_ARGS(&spExtCameraController)));

    // Use the IMFExtendedCameraController to check for support of a specific IMFExtendedCameraControl using GetExtendedCameraControl()

    return S_OK;
}
```

## -see-also

