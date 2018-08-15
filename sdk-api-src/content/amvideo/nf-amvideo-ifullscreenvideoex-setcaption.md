---
UID: NF:amvideo.IFullScreenVideoEx.SetCaption
title: IFullScreenVideoEx::SetCaption
author: windows-sdk-content
description: The SetCaption method sets the caption associated with the full-screen window.
old-location: dshow\ifullscreenvideoex_setcaption.htm
old-project: DirectShow
ms.assetid: 6f520ab4-867f-4001-8f2f-25f0d8efe454
ms.author: windowssdkdev
ms.date: 08/02/2018
ms.keywords: IFullScreenVideoEx interface [DirectShow],SetCaption method, IFullScreenVideoEx.SetCaption, IFullScreenVideoEx::SetCaption, IFullScreenVideoSetCaption, SetCaption, SetCaption method [DirectShow], SetCaption method [DirectShow],IFullScreenVideoEx interface, amvideo/IFullScreenVideoEx::SetCaption, dshow.ifullscreenvideoex_setcaption
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: amvideo.h
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
req.typenames: AMVAUncompDataInfo, *LPAMVAUncompDataInfo
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IFullScreenVideoEx.SetCaption
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
---

# IFullScreenVideoEx::SetCaption


## -description



The <code>SetCaption</code> method sets the caption associated with the full-screen window.




## -parameters




### -param strCaption [in]

String containing the caption.


## -returns



Returns an <b>HRESULT</b> value. Possible values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<b>NULL</b> pointer argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
</table>
 




## -remarks



The caption is visible when the window is minimized.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/4c9de58f-6ceb-4cf5-b1a5-d3e345e08190">IFullScreenVideoEx Interface</a>
 

 

