---
UID: NF:strmif.IAMVideoControl.SetMode
title: IAMVideoControl::SetMode (strmif.h)

description: The SetMode method sets the video control mode of operation.
old-location: dshow\iamvideocontrol_setmode.htm
tech.root: DirectShow
ms.assetid: 09fe5d3f-41d8-4a60-a770-64c628a6b82d

ms.date: 12/05/2018
ms.keywords: IAMVideoControl interface [DirectShow],SetMode method, IAMVideoControl.SetMode, IAMVideoControl::SetMode, IAMVideoControlSetMode, SetMode, SetMode method [DirectShow], SetMode method [DirectShow],IAMVideoControl interface, dshow.iamvideocontrol_setmode, strmif/IAMVideoControl::SetMode
ms.topic: method
f1_keywords: 
 - "strmif/IAMVideoControl.SetMode"
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
 - IAMVideoControl.SetMode
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAMVideoControl::SetMode


## -description



The <code>SetMode</code> method sets the video control mode of operation.




## -parameters




### -param pPin [in]

Pointer to the pin to set the video control mode on.


### -param Mode [in]

Value specifying a combination of the flags from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/strmif/ne-strmif-videocontrolflags">VideoControlFlags</a> enumeration to set the video control mode.


## -returns



Returns an <b>HRESULT</b> value that depends on the implementation of the interface.




## -remarks



Possible modes of operation include one or more of the following: flipping the picture horizontally, flipping the picture vertically, enabling external triggers, and simulating external triggers.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-iamvideocontrol">IAMVideoControl Interface</a>
 

 

