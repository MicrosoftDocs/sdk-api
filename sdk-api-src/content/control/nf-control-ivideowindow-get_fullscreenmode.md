---
UID: NF:control.IVideoWindow.get_FullScreenMode
title: IVideoWindow::get_FullScreenMode
author: windows-sdk-content
description: The get_FullScreenMode method queries whether the video renderer is in full-screen mode.
old-location: dshow\ivideowindow_get_fullscreenmode.htm
tech.root: DirectShow
ms.assetid: 742587c7-545a-4c5f-bff1-511ed6d0b1d5
ms.author: windowssdkdev
ms.date: 09/25/2018
ms.keywords: IVideoWindow interface [DirectShow],get_FullScreenMode method, IVideoWindow.get_FullScreenMode, IVideoWindow::get_FullScreenMode, IVideoWindowget_FullScreenMode, control/IVideoWindow::get_FullScreenMode, dshow.ivideowindow_get_fullscreenmode, get_FullScreenMode, get_FullScreenMode method [DirectShow], get_FullScreenMode method [DirectShow],IVideoWindow interface
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
 - IVideoWindow.get_FullScreenMode
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IVideoWindow::get_FullScreenMode


## -description



The <code>get_FullScreenMode</code> method queries whether the video renderer is in full-screen mode.




## -parameters




### -param FullScreenMode [out]

Receives the value OATRUE if the video renderer is in full-screen mode, or OAFALSE otherwise.
          


## -returns



Possible return values include the following:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
This filter does not support full-screen mode.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<b>NULL</b> pointer.

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
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_NOT_CONNECTED</b></dt>
</dl>
</td>
<td width="60%">
The video renderer filter is not connected.

</td>
</tr>
</table>
 




## -remarks



When the Filter Graph Manager is switching to full-screen mode, it calls this method to determine whether the current video renderer supports this mode. If the renderer does not have inherent support for full-screen playback, it should return E_NOTIMPL. If if does, it should return S_OK, and also return the correct value in the <i>FullScreenMode</i> parameter.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd375623(v=VS.85).aspx">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd377276(v=VS.85).aspx">IVideoWindow Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd377320(v=VS.85).aspx">IVideoWindow::put_FullScreenMode</a>
 

 

