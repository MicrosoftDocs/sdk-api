---
UID: NF:amvideo.IQualProp.get_AvgFrameRate
title: IQualProp::get_AvgFrameRate
author: windows-sdk-content
description: The get_AvgFrameRate method retrieves the actual average frame rate since streaming started.
old-location: dshow\iqualprop_get_avgframerate.htm
tech.root: DirectShow
ms.assetid: 31e326e2-56de-4c7c-b26a-836c9fc76342
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: IQualProp interface [DirectShow],get_AvgFrameRate method, IQualProp.get_AvgFrameRate, IQualProp::get_AvgFrameRate, IQualPropget_AvgFrameRate, amvideo/IQualProp::get_AvgFrameRate, dshow.iqualprop_get_avgframerate, get_AvgFrameRate, get_AvgFrameRate method [DirectShow], get_AvgFrameRate method [DirectShow],IQualProp interface
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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



The actual frame rate during playback might be less than the authored frame rate. For more information on actual versus authored frame rates, see the Remarks section for the <a href="https://msdn.microsoft.com/a175592b-0dc1-4001-b52f-785407965932">VIDEOINFOHEADER</a> structure.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/428dfb97-0dfa-442c-819e-291e6a58f712">IQualProp Interface</a>
 

 

