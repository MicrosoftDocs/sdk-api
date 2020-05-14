---
UID: NF:amvideo.IQualProp.get_AvgFrameRate
title: IQualProp::get_AvgFrameRate (amvideo.h)
description: The get_AvgFrameRate method retrieves the actual average frame rate since streaming started.helpviewer_keywords: ["IQualProp interface [DirectShow]","get_AvgFrameRate method","IQualProp.get_AvgFrameRate","IQualProp::get_AvgFrameRate","IQualPropget_AvgFrameRate","amvideo/IQualProp::get_AvgFrameRate","dshow.iqualprop_get_avgframerate","get_AvgFrameRate","get_AvgFrameRate method [DirectShow]","get_AvgFrameRate method [DirectShow]","IQualProp interface"]
old-location: dshow\iqualprop_get_avgframerate.htm
tech.root: DirectShow
ms.assetid: 31e326e2-56de-4c7c-b26a-836c9fc76342
ms.date: 12/05/2018
ms.keywords: IQualProp interface [DirectShow],get_AvgFrameRate method, IQualProp.get_AvgFrameRate, IQualProp::get_AvgFrameRate, IQualPropget_AvgFrameRate, amvideo/IQualProp::get_AvgFrameRate, dshow.iqualprop_get_avgframerate, get_AvgFrameRate, get_AvgFrameRate method [DirectShow], get_AvgFrameRate method [DirectShow],IQualProp interface
f1_keywords:
- amvideo/IQualProp.get_AvgFrameRate
dev_langs:
- c++
req.header: amvideo.h
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
- IQualProp.get_AvgFrameRate
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IQualProp::get_AvgFrameRate


## -description



The <code>get_AvgFrameRate</code> method retrieves the actual average frame rate since streaming started.




## -parameters




### -param piAvgFrameRate

Pointer to a variable that receives the actual number of frames per second, multiplied by 100. For example, an average frame rate of 30 frames per second will be represented as 3000.


## -returns



Returns an <b>HRESULT</b> value.




## -remarks



The actual frame rate during playback might be less than the authored frame rate. For more information on actual versus authored frame rates, see the Remarks section for the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader">VIDEOINFOHEADER</a> structure.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/amvideo/nn-amvideo-iqualprop">IQualProp Interface</a>
 

 

