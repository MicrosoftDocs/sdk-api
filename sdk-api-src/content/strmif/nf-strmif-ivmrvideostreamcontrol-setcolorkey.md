---
UID: NF:strmif.IVMRVideoStreamControl.SetColorKey
title: IVMRVideoStreamControl::SetColorKey
author: windows-sdk-content
description: The SetColorKey method sets the source color key that the VMR will use when compositing the video image.
old-location: dshow\ivmrvideostreamcontrol_setcolorkey.htm
tech.root: DirectShow
ms.assetid: 30a4009c-5da0-4a07-9d4b-7c9047fb6dd8
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: IVMRVideoStreamControl interface [DirectShow],SetColorKey method, IVMRVideoStreamControl.SetColorKey, IVMRVideoStreamControl::SetColorKey, IVMRVideoStreamControlSetColorKey, SetColorKey, SetColorKey method [DirectShow], SetColorKey method [DirectShow],IVMRVideoStreamControl interface, dshow.ivmrvideostreamcontrol_setcolorkey, strmif/IVMRVideoStreamControl::SetColorKey
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP1 [desktop apps only]
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
 - IVMRVideoStreamControl.SetColorKey
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- strmif.h
: 
- IVMRVideoStreamControl.SetColorKey
: 
---

# IVMRVideoStreamControl::SetColorKey


## -description



The <code>SetColorKey</code> method sets the source color key that the VMR will use when compositing the video image.




## -parameters




### -param lpClrKey

TBD




#### - clr [in]

Specifies the source color key as a <a href="https://msdn.microsoft.com/bd360860-94e3-4f91-a455-5fdb227368b3">DDCOLORKEY</a> type.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -see-also




<a href="https://msdn.microsoft.com/b42fa81e-99d7-4051-b909-2189581825d0">IVMRVideoStreamControl Interface</a>



<a href="https://msdn.microsoft.com/2075ac12-c799-4716-994f-46ff6928e670">IVMRVideoStreamControl::GetColorKey</a>



<a href="https://msdn.microsoft.com/3d0fdfac-ec7e-4e02-886b-2039c607dac7">Using the Video Mixing Renderer</a>
 

 

