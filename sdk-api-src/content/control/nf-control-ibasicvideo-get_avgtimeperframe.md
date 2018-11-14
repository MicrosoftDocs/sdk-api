---
UID: NF:control.IBasicVideo.get_AvgTimePerFrame
title: IBasicVideo::get_AvgTimePerFrame
author: windows-sdk-content
description: The get_AvgTimePerFrame method retrieves the average time between successive frames.
old-location: dshow\ibasicvideo_get_avgtimeperframe.htm
tech.root: DirectShow
ms.assetid: a32a1a46-cde3-401a-b933-c72e399e9ea1
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: IBasicVideo interface [DirectShow],get_AvgTimePerFrame method, IBasicVideo.get_AvgTimePerFrame, IBasicVideo::get_AvgTimePerFrame, IBasicVideoget_AvgTimePerFrame, control/IBasicVideo::get_AvgTimePerFrame, dshow.ibasicvideo_get_avgtimeperframe, get_AvgTimePerFrame, get_AvgTimePerFrame method [DirectShow], get_AvgTimePerFrame method [DirectShow],IBasicVideo interface
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: control.h
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
 - IBasicVideo.get_AvgTimePerFrame
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- control.h
: 
- IBasicVideo.get_AvgTimePerFrame
: 
---

# IBasicVideo::get_AvgTimePerFrame


## -description



The <code>get_AvgTimePerFrame</code> method retrieves the average time between successive frames.




## -parameters




### -param pAvgTimePerFrame [out]

Pointer to a variable of type <a href="https://msdn.microsoft.com/0c5eed92-9f98-49ed-aab0-5958ee574fe9">REFTIME</a> that receives the average frame time, in seconds.


## -returns



Returns an <b>HRESULT</b> value.




## -remarks



This method returns the authored time per frame. This value is typically set by the source filter, which obtains it from information in the video stream itself. This value is not necessarily equal to the actual time per frame at which the video is rendered.

To retrieve the actual frame rate during playback, use the <a href="https://msdn.microsoft.com/en-us/library/Dd376916(v=VS.85).aspx">IQualProp::get_AvgFrameRate</a>. For more information on actual versus authored frame rates, see the Remarks section for the <a href="https://msdn.microsoft.com/en-us/library/Dd407325(v=VS.85).aspx">VIDEOINFOHEADER</a> structure.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd375623(v=VS.85).aspx">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd389540(v=VS.85).aspx">IBasicVideo Interface</a>
 

 

