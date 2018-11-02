---
UID: NF:amvideo.IFullScreenVideoEx.GetMessageDrain
title: IFullScreenVideoEx::GetMessageDrain
author: windows-sdk-content
description: The GetMessageDrain method retrieves the window that receives mouse and keyboard messages, if any.
old-location: dshow\ifullscreenvideoex_getmessagedrain.htm
tech.root: DirectShow
ms.assetid: c1a83ad9-be4b-4adf-a316-d5dfb3df05ef
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: GetMessageDrain, GetMessageDrain method [DirectShow], GetMessageDrain method [DirectShow],IFullScreenVideoEx interface, IFullScreenVideoEx interface [DirectShow],GetMessageDrain method, IFullScreenVideoEx.GetMessageDrain, IFullScreenVideoEx::GetMessageDrain, IFullScreenVideoGetMessageDrain, amvideo/IFullScreenVideoEx::GetMessageDrain, dshow.ifullscreenvideoex_getmessagedrain
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IFullScreenVideoEx.GetMessageDrain
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFullScreenVideoEx::GetMessageDrain


## -description



The <code>GetMessageDrain</code> method retrieves the window that receives mouse and keyboard messages, if any.




## -parameters




### -param hwnd [out]

Pointer to a variable that receives the handle of the window. If no window has been designated to receive messages, this parameter receives the value <b>NULL</b>.


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



This method is equivalent to the <a href="https://msdn.microsoft.com/9a1a3070-5b68-4dd2-bc10-97a8331cc262">IVideoWindow::get_MessageDrain</a> method.

The Full Screen video renderer posts all mouse and keyboard messages to the window designated as a message drain. The exact list of messages that are posted is the same as the list given in <a href="https://msdn.microsoft.com/aaf8624c-b3ea-4034-845a-6cd74c725c44">IVideoWindow::put_MessageDrain</a>.

Applications do not need to use this method. Use the <a href="https://msdn.microsoft.com/9a1a3070-5b68-4dd2-bc10-97a8331cc262">IVideoWindow::get_MessageDrain</a> method on the Filter Graph Manager instead.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/4c9de58f-6ceb-4cf5-b1a5-d3e345e08190">IFullScreenVideoEx Interface</a>
 

 

