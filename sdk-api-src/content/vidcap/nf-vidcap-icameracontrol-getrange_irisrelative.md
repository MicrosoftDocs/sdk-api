---
UID: NF:vidcap.ICameraControl.getRange_IrisRelative
title: ICameraControl::getRange_IrisRelative (vidcap.h)
author: windows-sdk-content
description: The getRange_IrisRelative method returns the range of relative aperture settings supported by the camera. The relative aperture is expressed as a number of steps, where the size of each step depends on the camera model.
old-location: dshow\icameracontrol_getrange_irisrelative.htm
tech.root: DirectShow
ms.assetid: 9816e29b-3366-49e7-aa4c-46b06963c176
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ICameraControl interface [DirectShow],getRange_IrisRelative method, ICameraControl.getRange_IrisRelative, ICameraControl::getRange_IrisRelative, ICameraControlgetRange_IrisRelative, dshow.icameracontrol_getrange_irisrelative, getRange_IrisRelative, getRange_IrisRelative method [DirectShow], getRange_IrisRelative method [DirectShow],ICameraControl interface, vidcap/ICameraControl::getRange_IrisRelative
ms.topic: method
req.header: vidcap.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Strmiids.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - ICameraControl.getRange_IrisRelative
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ICameraControl::getRange_IrisRelative


## -description


The <code>getRange_IrisRelative</code> method returns the range of relative aperture settings supported by the camera. The relative aperture is expressed as a number of steps, where the size of each step depends on the camera model.


## -parameters




### -param pMin [out]

Receives the minimum relative aperture setting.


### -param pMax [out]

Receives the maximum relative aperture setting.


### -param pSteppingDelta [out]

Receives the smallest step between settings.


### -param pDefault [out]

Receives the default relative aperture setting.


### -param pCapsFlag [out]

Receives one or more flags. See <a href="https://docs.microsoft.com/windows/desktop/api/strmif/ne-strmif-tagcameracontrolflags">CameraControlFlags</a>.


## -returns



Returns an <b>HRESULT</b> value.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/vidcap/nn-vidcap-icameracontrol">ICameraControl Interface</a>
 

 

