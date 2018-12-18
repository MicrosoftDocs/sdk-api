---
UID: NF:vidcap.ICameraControl.get_Zoom
title: ICameraControl::get_Zoom
author: windows-sdk-content
description: The get_Zoom method returns the camera's optical zoom level.
old-location: dshow\icameracontrol_get_zoom.htm
tech.root: DirectShow
ms.assetid: 7c1fe500-bccf-46ed-bcd9-f65b25e8ccb7
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ICameraControl interface [DirectShow],get_Zoom method, ICameraControl.get_Zoom, ICameraControl::get_Zoom, ICameraControlget_Zoom, dshow.icameracontrol_get_zoom, get_Zoom, get_Zoom method [DirectShow], get_Zoom method [DirectShow],ICameraControl interface, vidcap/ICameraControl::get_Zoom
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
 - ICameraControl.get_Zoom
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICameraControl::get_Zoom


## -description


The <code>get_Zoom</code> method returns the camera's optical zoom level.


## -parameters




### -param pValue [out]

Receives the zoom level. The units for this setting are not defined. For information about calculating magnification from zoom level, see <a href="https://msdn.microsoft.com/en-us/library/Dd376315(v=VS.85).aspx">ICameraControl::get_FocalLengths</a>.


### -param pFlags [out]

Receives one or more flags. See <a href="https://msdn.microsoft.com/en-us/library/Dd318251(v=VS.85).aspx">CameraControlFlags</a>.


## -returns



Returns an <b>HRESULT</b> value.




## -remarks



This method returns the optical zoom level only. To get the digital zoom level, call <a href="https://msdn.microsoft.com/en-us/library/Dd377254(v=VS.85).aspx">IVideoProcAmp::get_DigitalMultiplier</a>.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd376298(v=VS.85).aspx">ICameraControl Interface</a>
 

 

