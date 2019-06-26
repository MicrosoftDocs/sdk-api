---
UID: NF:vidcap.ICameraControl.put_Zoom
title: ICameraControl::put_Zoom (vidcap.h)
author: windows-sdk-content
description: The put_Zoom method sets the camera's zoom level.
old-location: dshow\icameracontrol_put_zoom.htm
tech.root: DirectShow
ms.assetid: e6bb0206-04c4-4d93-b267-2881e58c0a14
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ICameraControl interface [DirectShow],put_Zoom method, ICameraControl.put_Zoom, ICameraControl::put_Zoom, ICameraControlput_Zoom, dshow.icameracontrol_put_zoom, put_Zoom, put_Zoom method [DirectShow], put_Zoom method [DirectShow],ICameraControl interface, vidcap/ICameraControl::put_Zoom
ms.topic: method
f1_keywords: 
 - "vidcap/ICameraControl.put_Zoom"
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
 - ICameraControl.put_Zoom
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ICameraControl::put_Zoom


## -description


The <code>put_Zoom</code> method sets the camera's zoom level.


## -parameters




### -param Value [in]

Specifies the zoom level. The units for this setting are not defined. For information about calculating magnification from zoom level, see <a href="https://docs.microsoft.com/windows/desktop/api/vidcap/nf-vidcap-icameracontrol-get_focallengths">ICameraControl::get_FocalLengths</a>.


### -param Flags [in]

Zero or more flags. See <a href="https://docs.microsoft.com/windows/desktop/api/strmif/ne-strmif-tagcameracontrolflags">CameraControlFlags</a>. If the CameraControl_Flags_Auto flag is used, the <i>Value</i> parameter is ignored and the camera sets the default value.


## -returns



Returns an <b>HRESULT</b> value.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/vidcap/nn-vidcap-icameracontrol">ICameraControl Interface</a>
 

 

