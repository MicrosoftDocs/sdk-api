---
UID: NF:control.IBasicVideo.GetSourcePosition
title: IBasicVideo::GetSourcePosition
author: windows-sdk-content
description: The GetSourcePosition method retrieves the position of the source rectangle.
old-location: dshow\ibasicvideo_getsourceposition.htm
tech.root: DirectShow
ms.assetid: 4624e38c-63ff-4860-a899-c70e44e0f8aa
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetSourcePosition, GetSourcePosition method [DirectShow], GetSourcePosition method [DirectShow],IBasicVideo interface, IBasicVideo interface [DirectShow],GetSourcePosition method, IBasicVideo.GetSourcePosition, IBasicVideo::GetSourcePosition, IBasicVideoGetSourcePosition, control/IBasicVideo::GetSourcePosition, dshow.ibasicvideo_getsourceposition
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
 - IBasicVideo.GetSourcePosition
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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



This method has the same effect as individually calling the <a href="https://msdn.microsoft.com/en-us/library/Dd389583(v=VS.85).aspx">IBasicVideo::get_SourceLeft</a>, <a href="https://msdn.microsoft.com/en-us/library/Dd389584(v=VS.85).aspx">IBasicVideo::get_SourceTop</a>, <a href="https://msdn.microsoft.com/en-us/library/Dd389585(v=VS.85).aspx">IBasicVideo::get_SourceWidth</a>, and <a href="https://msdn.microsoft.com/en-us/library/Dd389582(v=VS.85).aspx">IBasicVideo::get_SourceHeight</a> methods.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd375623(v=VS.85).aspx">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd389540(v=VS.85).aspx">IBasicVideo Interface</a>
 

 

