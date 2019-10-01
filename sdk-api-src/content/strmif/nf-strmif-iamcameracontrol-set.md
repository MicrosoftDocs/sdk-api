---
UID: NF:strmif.IAMCameraControl.Set
title: IAMCameraControl::Set (strmif.h)
author: windows-sdk-content
description: The Set method sets a specified property on the camera.
old-location: dshow\iamcameracontrol_set.htm
tech.root: DirectShow
ms.assetid: d896fb5e-a43b-4cb8-a5d1-4ce6e60831be
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IAMCameraControl interface [DirectShow],Set method, IAMCameraControl.Set, IAMCameraControl::Set, IAMCameraControlSet, Set, Set method [DirectShow], Set method [DirectShow],IAMCameraControl interface, dshow.iamcameracontrol_set, strmif/IAMCameraControl::Set
ms.topic: method
f1_keywords: 
 - "strmif/IAMCameraControl.Set"
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - IAMCameraControl.Set
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAMCameraControl::Set


## -description



The <b>Set</b> method sets a specified property on the camera.




## -parameters




### -param Property [in]

Specifies the property to set, as a value from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/strmif/ne-strmif-cameracontrolproperty">CameraControlProperty</a> enumeration.
          


### -param lValue [in]

Specifies the new value of the property.
          


### -param Flags [in]

Specifies the desired control setting, as a member of the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/strmif/ne-strmif-cameracontrolflags">CameraControlFlags</a> enumeration.
          


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



If the <i>Flags</i> parameter is <b>CameraControl_Flags_Auto</b>, the method ignores the <i>lValue</i> parameter.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/configure-the-video-quality">Configure the Video Quality</a>



<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-iamcameracontrol">IAMCameraControl Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iamcameracontrol-get">IAMCameraControl::Get</a>
 

 

