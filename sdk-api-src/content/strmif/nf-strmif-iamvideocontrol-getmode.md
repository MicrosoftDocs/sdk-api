---
UID: NF:strmif.IAMVideoControl.GetMode
title: IAMVideoControl::GetMode (strmif.h)
description: The GetMode method retrieves the video control mode of operation.
old-location: dshow\iamvideocontrol_getmode.htm
tech.root: DirectShow
ms.assetid: 4b937661-67b2-445c-ab25-8655e1036797
ms.date: 12/05/2018
ms.keywords: GetMode, GetMode method [DirectShow], GetMode method [DirectShow],IAMVideoControl interface, IAMVideoControl interface [DirectShow],GetMode method, IAMVideoControl.GetMode, IAMVideoControl::GetMode, IAMVideoControlGetMode, dshow.iamvideocontrol_getmode, strmif/IAMVideoControl::GetMode
ms.topic: method
f1_keywords:
- strmif/IAMVideoControl.GetMode
dev_langs:
- c++
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
- IAMVideoControl.GetMode
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAMVideoControl::GetMode


## -description



The <code>GetMode</code> method retrieves the video control mode of operation.




## -parameters




### -param pPin [in]

Pointer to the pin to retrieve the video control mode from.


### -param Mode [out]

Pointer to a value representing a combination of the flags from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/strmif/ne-strmif-videocontrolflags">VideoControlFlags</a> enumeration, which specify the video control mode.


## -returns



Returns an <b>HRESULT</b> value that depends on the implementation of the interface.




## -remarks



Possible modes of operation include one or more of the following: flipping the picture horizontally, flipping the picture vertically, enabling external triggers, and simulating external triggers.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-iamvideocontrol">IAMVideoControl Interface</a>
 

 

