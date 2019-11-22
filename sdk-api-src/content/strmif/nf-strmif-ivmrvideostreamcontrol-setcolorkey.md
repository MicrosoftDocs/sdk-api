---
UID: NF:strmif.IVMRVideoStreamControl.SetColorKey
title: IVMRVideoStreamControl::SetColorKey (strmif.h)

description: The SetColorKey method sets the source color key that the VMR will use when compositing the video image.
old-location: dshow\ivmrvideostreamcontrol_setcolorkey.htm
tech.root: DirectShow
ms.assetid: 30a4009c-5da0-4a07-9d4b-7c9047fb6dd8

ms.date: 12/05/2018
ms.keywords: IVMRVideoStreamControl interface [DirectShow],SetColorKey method, IVMRVideoStreamControl.SetColorKey, IVMRVideoStreamControl::SetColorKey, IVMRVideoStreamControlSetColorKey, SetColorKey, SetColorKey method [DirectShow], SetColorKey method [DirectShow],IVMRVideoStreamControl interface, dshow.ivmrvideostreamcontrol_setcolorkey, strmif/IVMRVideoStreamControl::SetColorKey
ms.topic: method
f1_keywords: 
 - "strmif/IVMRVideoStreamControl.SetColorKey"
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
 - IVMRVideoStreamControl.SetColorKey
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IVMRVideoStreamControl::SetColorKey


## -description



The <code>SetColorKey</code> method sets the source color key that the VMR will use when compositing the video image.




## -parameters




### -param lpClrKey [in]

Specifies the source color key as a <a href="https://docs.microsoft.com/windows/desktop/api/strmif/ns-strmif-ddcolorkey">DDCOLORKEY</a> type.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-ivmrvideostreamcontrol">IVMRVideoStreamControl Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-ivmrvideostreamcontrol-getcolorkey">IVMRVideoStreamControl::GetColorKey</a>



<a href="https://docs.microsoft.com/windows/desktop/DirectShow/using-the-video-mixing-renderer">Using the Video Mixing Renderer</a>
 

 

