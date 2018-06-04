---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
 

 

