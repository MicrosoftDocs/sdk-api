---
UID: NF:control.IBasicVideo.SetSourcePosition
title: IBasicVideo::SetSourcePosition
author: windows-sdk-content
description: The SetSourcePosition method sets the source rectangle.
old-location: dshow\ibasicvideo_setsourceposition.htm
old-project: DirectShow
ms.assetid: afe78775-f2b0-4d10-a702-f0329fe79c6d
ms.author: windowssdkdev
ms.date: 08/02/2018
ms.keywords: IBasicVideo interface [DirectShow],SetSourcePosition method, IBasicVideo.SetSourcePosition, IBasicVideo::SetSourcePosition, IBasicVideoSetSourcePosition, SetSourcePosition, SetSourcePosition method [DirectShow], SetSourcePosition method [DirectShow],IBasicVideo interface, control/IBasicVideo::SetSourcePosition, dshow.ibasicvideo_setsourceposition
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: control.h
req.include-header: Dshow.h
req.redist: 
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
tech.root: 
req.typenames: WMPContextMenuInfo
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
req.lib: Strmiids.lib
req.dll: 
req.irql: 
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



This method has the same effect as individually calling the <a href="https://msdn.microsoft.com/en-us/library/Dd389595(v=VS.85).aspx">IBasicVideo::put_SourceLeft</a>, <a href="https://msdn.microsoft.com/en-us/library/Dd389596(v=VS.85).aspx">IBasicVideo::put_SourceTop</a>, <a href="https://msdn.microsoft.com/en-us/library/Dd389597(v=VS.85).aspx">IBasicVideo::put_SourceWidth</a>, and <a href="https://msdn.microsoft.com/en-us/library/Dd389594(v=VS.85).aspx">IBasicVideo::put_SourceHeight</a> methods.

Setting this coordinate does not affect the destination rectangle height.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd375623(v=VS.85).aspx">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd389540(v=VS.85).aspx">IBasicVideo Interface</a>
 

 

