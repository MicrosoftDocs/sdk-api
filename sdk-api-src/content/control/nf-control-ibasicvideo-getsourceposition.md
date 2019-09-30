---
UID: NF:control.IBasicVideo.GetSourcePosition
title: IBasicVideo::GetSourcePosition (control.h)
author: windows-sdk-content
description: The GetSourcePosition method retrieves the position of the source rectangle.
old-location: dshow\ibasicvideo_getsourceposition.htm
tech.root: DirectShow
ms.assetid: 4624e38c-63ff-4860-a899-c70e44e0f8aa
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetSourcePosition, GetSourcePosition method [DirectShow], GetSourcePosition method [DirectShow],IBasicVideo interface, IBasicVideo interface [DirectShow],GetSourcePosition method, IBasicVideo.GetSourcePosition, IBasicVideo::GetSourcePosition, IBasicVideoGetSourcePosition, control/IBasicVideo::GetSourcePosition, dshow.ibasicvideo_getsourceposition
ms.topic: method
f1_keywords: 
 - "control/IBasicVideo.GetSourcePosition"
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
 - IBasicVideo.GetSourcePosition
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IBasicVideo::GetSourcePosition


## -description



The <code>GetSourcePosition</code> method retrieves the position of the source rectangle.




## -parameters




### -param pLeft [out]

Pointer to a variable that receives the x-coordinate, in pixels.


### -param pTop [out]

Pointer to a variable that receives the y-coordinate, in pixels.


### -param pWidth [out]

Pointer to a variable that receives the width, in pixels.


### -param pHeight [out]

Pointer to a variable that receives the height, in pixels.


## -returns



Returns an <b>HRESULT</b> value.




## -remarks



This method has the same effect as individually calling the <a href="https://docs.microsoft.com/windows/desktop/api/control/nf-control-ibasicvideo-get_sourceleft">IBasicVideo::get_SourceLeft</a>, <a href="https://docs.microsoft.com/windows/desktop/api/control/nf-control-ibasicvideo-get_sourcetop">IBasicVideo::get_SourceTop</a>, <a href="https://docs.microsoft.com/windows/desktop/api/control/nf-control-ibasicvideo-get_sourcewidth">IBasicVideo::get_SourceWidth</a>, and <a href="https://docs.microsoft.com/windows/desktop/api/control/nf-control-ibasicvideo-get_sourceheight">IBasicVideo::get_SourceHeight</a> methods.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/control/nn-control-ibasicvideo">IBasicVideo Interface</a>
 

 

