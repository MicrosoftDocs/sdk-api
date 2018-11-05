---
UID: NF:strmif.IVMRImageCompositor.SetStreamMediaType
title: IVMRImageCompositor::SetStreamMediaType
author: windows-sdk-content
description: The SetStreamMediaType method sets the media type for the input stream.
old-location: dshow\ivmrimagecompositor_setstreammediatype.htm
tech.root: DirectShow
ms.assetid: ea3ed291-d837-4d11-bc82-0a060b093b21
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: IVMRImageCompositor interface [DirectShow],SetStreamMediaType method, IVMRImageCompositor.SetStreamMediaType, IVMRImageCompositor::SetStreamMediaType, IVMRImageCompositorSetStreamMediaType, SetStreamMediaType, SetStreamMediaType method [DirectShow], SetStreamMediaType method [DirectShow],IVMRImageCompositor interface, dshow.ivmrimagecompositor_setstreammediatype, strmif/IVMRImageCompositor::SetStreamMediaType
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
 - IVMRImageCompositor.SetStreamMediaType
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IVMRImageCompositor::SetStreamMediaType


## -description



The <code>SetStreamMediaType</code> method sets the media type for the input stream.




## -parameters




### -param dwStrmID

Specifies the input stream. The value must be from 1 through 16.


### -param pmt

Pointer to an <a href="https://msdn.microsoft.com/973697d0-2897-48b5-88ca-a88a9650eb02">AM_MEDIA_TYPE</a> structure that specifies the media type.


### -param fTexture

If <b>TRUE</b>, specifies that the target surface is a Direct3D texture surface.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/d905e871-c156-4140-bb3f-a19fa0cd79be">IVMRImageCompositor Interface</a>



<a href="https://msdn.microsoft.com/3d0fdfac-ec7e-4e02-886b-2039c607dac7">Using the Video Mixing Renderer</a>
 

 

