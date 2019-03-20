---
UID: NF:strmif.IAMVideoControl.GetCurrentActualFrameRate
title: IAMVideoControl::GetCurrentActualFrameRate (strmif.h)
author: windows-sdk-content
description: The GetCurrentActualFrameRate method retrieves the actual frame rate, expressed as a frame duration in 100-nanosecond units.
old-location: dshow\iamvideocontrol_getcurrentactualframerate.htm
tech.root: DirectShow
ms.assetid: 373cabed-af09-4d54-b4e1-0ef87727430a
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetCurrentActualFrameRate, GetCurrentActualFrameRate method [DirectShow], GetCurrentActualFrameRate method [DirectShow],IAMVideoControl interface, IAMVideoControl interface [DirectShow],GetCurrentActualFrameRate method, IAMVideoControl.GetCurrentActualFrameRate, IAMVideoControl::GetCurrentActualFrameRate, IAMVideoControlGetCurrentActualFrameRate, dshow.iamvideocontrol_getcurrentactualframerate, strmif/IAMVideoControl::GetCurrentActualFrameRate
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
 - IAMVideoControl.GetCurrentActualFrameRate
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAMVideoControl::GetCurrentActualFrameRate


## -description



The <code>GetCurrentActualFrameRate</code> method retrieves the actual frame rate, expressed as a frame duration in 100-nanosecond units. USB (Universal Serial Bus) and IEEE 1394 cameras may provide lower frame rates than requested because of bandwidth availability. This is only available during video streaming.




## -parameters




### -param pPin [in]

Pointer to the pin to retrieve the frame rate from.


### -param ActualFrameRate [out]

Pointer to the frame rate in frame duration in 100-nanosecond units.


## -returns



Returns an <b>HRESULT</b> value that depends on the implementation of the interface.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/bd114977-c76c-4429-a835-98601b350a93">IAMVideoControl Interface</a>
 

 

