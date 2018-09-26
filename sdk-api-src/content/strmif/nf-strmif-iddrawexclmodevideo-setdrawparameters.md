---
UID: NF:strmif.IDDrawExclModeVideo.SetDrawParameters
title: IDDrawExclModeVideo::SetDrawParameters
author: windows-sdk-content
description: The SetDrawParameters method specifies which part of the original video will appear at which position of the screen.
old-location: dshow\iddrawexclmodevideo_setdrawparameters.htm
tech.root: DirectShow
ms.assetid: e5c2eda5-4276-4906-8098-37bba3fd4e5a
ms.author: windowssdkdev
ms.date: 09/25/2018
ms.keywords: IDDrawExclModeVideo interface [DirectShow],SetDrawParameters method, IDDrawExclModeVideo.SetDrawParameters, IDDrawExclModeVideo::SetDrawParameters, IDDrawExclModeVideoSetDrawParameters, SetDrawParameters, SetDrawParameters method [DirectShow], SetDrawParameters method [DirectShow],IDDrawExclModeVideo interface, dshow.iddrawexclmodevideo_setdrawparameters, strmif/IDDrawExclModeVideo::SetDrawParameters
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IDDrawExclModeVideo.SetDrawParameters
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDDrawExclModeVideo::SetDrawParameters


## -description



The <code>SetDrawParameters</code> method specifies which part of the original video will appear at which position of the screen.




## -parameters




### -param prcSource

TBD


### -param prcTarget

TBD




#### - pDestRect [in]

Pointer to the <b>RECT</b> that indicates where the video will appear on the screen.


#### - pSrcRect [in]

Pointer to the <b>RECT</b> structure of the original video.


## -returns



Returns an <b>HRESULT</b> value that depends on the implementation of the interface.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/6a846a07-f513-49e7-85e8-192a5c211515">IDDrawExclModeVideo Interface</a>



<a href="https://msdn.microsoft.com/7f22d4cd-93e0-4d7d-b8f3-932488d2c672">IDDrawExclModeVideoCallback Interface</a>
 

 

