---
UID: NF:amvideo.IFullScreenVideoEx.SetMonitor
title: IFullScreenVideoEx::SetMonitor
author: windows-sdk-content
description: The SetMonitor method specifies which monitor to use. The Full Screen Renderer only supports the primary monitor, however, so this method is not useful in the current implementation.
old-location: dshow\ifullscreenvideoex_setmonitor.htm
old-project: DirectShow
ms.assetid: f2db1009-ce5b-4ebe-becb-bed3d1187335
ms.author: windowssdkdev
ms.date: 07/09/2018
ms.keywords: IFullScreenVideoEx interface [DirectShow],SetMonitor method, IFullScreenVideoEx.SetMonitor, IFullScreenVideoEx::SetMonitor, IFullScreenVideoSetMonitor, SetMonitor, SetMonitor method [DirectShow], SetMonitor method [DirectShow],IFullScreenVideoEx interface, amvideo/IFullScreenVideoEx::SetMonitor, dshow.ifullscreenvideoex_setmonitor
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: amvideo.h
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
 - IFullScreenVideoEx.SetMonitor
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
---

# IFullScreenVideoEx::SetMonitor


## -description



The <code>SetMonitor</code> method specifies which monitor to use. The Full Screen Renderer only supports the primary monitor, however, so this method is not useful in the current implementation.




## -parameters




### -param Monitor [in]

Specifies the index of the monitor to use. Must be zero in the current implementation.


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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid argument.

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
 




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/4c9de58f-6ceb-4cf5-b1a5-d3e345e08190">IFullScreenVideoEx Interface</a>
 

 

