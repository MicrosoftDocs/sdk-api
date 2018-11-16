---
UID: NF:control.IBasicVideo.SetSourcePosition
title: IBasicVideo::SetSourcePosition
author: windows-sdk-content
description: The SetSourcePosition method sets the source rectangle.
old-location: dshow\ibasicvideo_setsourceposition.htm
tech.root: DirectShow
ms.assetid: afe78775-f2b0-4d10-a702-f0329fe79c6d
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IBasicVideo interface [DirectShow],SetSourcePosition method, IBasicVideo.SetSourcePosition, IBasicVideo::SetSourcePosition, IBasicVideoSetSourcePosition, SetSourcePosition, SetSourcePosition method [DirectShow], SetSourcePosition method [DirectShow],IBasicVideo interface, control/IBasicVideo::SetSourcePosition, dshow.ibasicvideo_setsourceposition
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
 - IBasicVideo.SetSourcePosition
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
- IBasicVideo.SetSourcePosition
: 
---

# IBasicVideo::SetSourcePosition


## -description



The <code>SetSourcePosition</code> method sets the source rectangle.




## -parameters




### -param Left [in]

Specifies the x-coordinate, in pixels.


### -param Top [in]

Specifies the y-coordinate, in pixels.


### -param Width [in]

Specifies the width, in pixels.


### -param Height [in]

Specifies the height, in pixels.


## -returns



Returns an <b>HRESULT</b> value.




## -remarks



This method has the same effect as individually calling the <a href="https://msdn.microsoft.com/0388d5fe-5434-41b9-b005-c0e4bf36bb27">IBasicVideo::put_SourceLeft</a>, <a href="https://msdn.microsoft.com/0a76518d-f79d-45ef-8e19-a3e5ee1e4db0">IBasicVideo::put_SourceTop</a>, <a href="https://msdn.microsoft.com/0747a1fb-42b6-452f-8a92-eb87931c004c">IBasicVideo::put_SourceWidth</a>, and <a href="https://msdn.microsoft.com/d8cb4ae1-cbbf-44cb-9387-770ee95280a1">IBasicVideo::put_SourceHeight</a> methods.

Setting this coordinate does not affect the destination rectangle height.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/14f45bdc-2271-459d-b165-c860c8fc3e0b">IBasicVideo Interface</a>
 

 

