---
UID: NF:strmif.IAMCameraControl.Get
title: IAMCameraControl::Get (strmif.h)
author: windows-sdk-content
description: The Get method gets the current setting of a camera property.
old-location: dshow\iamcameracontrol_get.htm
tech.root: DirectShow
ms.assetid: 5a21f207-5fbb-44b2-82d2-89be29dbdf2c
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: Get, Get method [DirectShow], Get method [DirectShow],IAMCameraControl interface, IAMCameraControl interface [DirectShow],Get method, IAMCameraControl.Get, IAMCameraControl::Get, IAMCameraControlGet, dshow.iamcameracontrol_get, strmif/IAMCameraControl::Get
ms.topic: method
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
 - IAMCameraControl.Get
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAMCameraControl::Get


## -description



The <b>Get</b> method gets the current setting of a camera property.




## -parameters




### -param Property [in]

Specifies the property to retrieve, as a value from the <a href="https://docs.microsoft.com/windows/desktop/api/strmif/ne-strmif-tagcameracontrolproperty">CameraControlProperty</a> enumeration.
          


### -param lValue [out]

Receives the value of the property.
          


### -param Flags [out]

Receives a member of the <a href="https://docs.microsoft.com/windows/desktop/api/strmif/ne-strmif-tagcameracontrolflags">CameraControlFlags</a> enumeration. The returned value indicates whether the setting is controlled manually or automatically.
          


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/configure-the-video-quality">Configure the Video Quality</a>



<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-iamcameracontrol">IAMCameraControl Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iamcameracontrol-set">IAMCameraControl::Set</a>
 

 

