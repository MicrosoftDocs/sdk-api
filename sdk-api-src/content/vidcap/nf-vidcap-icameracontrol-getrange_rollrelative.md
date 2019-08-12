---
UID: NF:vidcap.ICameraControl.getRange_RollRelative
title: ICameraControl::getRange_RollRelative (vidcap.h)
author: windows-sdk-content
description: The getRange_RollRelative method returns the range of relative roll angles supported by the camera. The relative roll is expressed as a number of steps, where the size of each step depends on the camera model.
old-location: dshow\icameracontrol_getrange_rollrelative.htm
tech.root: DirectShow
ms.assetid: c0208111-8648-4511-99f6-20489a026c91
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ICameraControl interface [DirectShow],getRange_RollRelative method, ICameraControl.getRange_RollRelative, ICameraControl::getRange_RollRelative, ICameraControlgetRange_RollRelative, dshow.icameracontrol_getrange_rollrelative, getRange_RollRelative, getRange_RollRelative method [DirectShow], getRange_RollRelative method [DirectShow],ICameraControl interface, vidcap/ICameraControl::getRange_RollRelative
ms.topic: method
f1_keywords: 
 - "vidcap/ICameraControl.getRange_RollRelative"
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
 - ICameraControl.getRange_RollRelative
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ICameraControl::getRange_RollRelative


## -description


The <code>getRange_RollRelative</code> method returns the range of relative roll angles supported by the camera. The relative roll is expressed as a number of steps, where the size of each step depends on the camera model.


## -parameters




### -param pMin [out]

Receives the minimum relative roll angle.


### -param pMax [out]

Receives the maximum relative roll angle.


### -param pSteppingDelta [out]

Receives the smallest step between settings.


### -param pDefault [out]

Receives the default relative roll angle.


### -param pCapsFlag [out]

Receives one or more flags. See <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/strmif/ne-strmif-cameracontrolflags">CameraControlFlags</a>.


## -returns



Returns an <b>HRESULT</b> value.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/vidcap/nn-vidcap-icameracontrol">ICameraControl Interface</a>
 

 

