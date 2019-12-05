---
UID: NF:strmif.IVMRVideoStreamControl.GetColorKey
title: IVMRVideoStreamControl::GetColorKey (strmif.h)
description: The GetColorKey method retrieves the source color key currently set for this stream.
old-location: dshow\ivmrvideostreamcontrol_getcolorkey.htm
tech.root: DirectShow
ms.assetid: 2075ac12-c799-4716-994f-46ff6928e670
ms.date: 12/05/2018
ms.keywords: GetColorKey, GetColorKey method [DirectShow], GetColorKey method [DirectShow],IVMRVideoStreamControl interface, IVMRVideoStreamControl interface [DirectShow],GetColorKey method, IVMRVideoStreamControl.GetColorKey, IVMRVideoStreamControl::GetColorKey, IVMRVideoStreamControlGetColorKey, dshow.ivmrvideostreamcontrol_getcolorkey, strmif/IVMRVideoStreamControl::GetColorKey
ms.topic: method
f1_keywords:
- strmif/IVMRVideoStreamControl.GetColorKey
dev_langs:
- c++
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
- IVMRVideoStreamControl.GetColorKey
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IVMRVideoStreamControl::GetColorKey


## -description



The <code>GetColorKey</code> method retrieves the source color key currently set for this stream.




## -parameters




### -param lpClrKey [out]

Address of a <a href="https://docs.microsoft.com/windows/desktop/api/strmif/ns-strmif-ddcolorkey">DDCOLORKEY</a> structure that receives the source color key.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-ivmrvideostreamcontrol">IVMRVideoStreamControl Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-ivmrvideostreamcontrol-setcolorkey">IVMRVideoStreamControl::SetColorKey</a>



<a href="https://docs.microsoft.com/windows/desktop/DirectShow/using-the-video-mixing-renderer">Using the Video Mixing Renderer</a>
 

 

