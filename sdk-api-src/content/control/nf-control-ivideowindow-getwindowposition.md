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

# IVideoWindow::GetWindowPosition


## -description



The <code>GetWindowPosition</code> method retrieves the position of the video window.




## -parameters




### -param pLeft [out]

Receives the x-coordinate, in pixels.


### -param pTop [out]

Receives the y-coordinate, in pixels.


### -param pWidth [out]

Receives the width of the window, in pixels.
          


### -param pHeight [out]

Receives the height of the window, in pixels.
          


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



This method has the same effect as calling the <a href="https://msdn.microsoft.com/6d75c926-588c-4fb2-b537-f27602799b2e">IVideoWindow::get_Left</a>, <a href="https://msdn.microsoft.com/00baab45-d740-4f74-bd53-eb2ff21c5dcc">IVideoWindow::get_Top</a>, <a href="https://msdn.microsoft.com/179b065a-7269-40fa-8772-b336f27d69de">IVideoWindow::get_Width</a>, and <a href="https://msdn.microsoft.com/c1d29cd5-1e82-4406-b007-aa7b581d158e">IVideoWindow::get_Height</a> methods.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/8e931c15-bd1d-409e-ada1-97fe49125fe7">IVideoWindow Interface</a>



<a href="https://msdn.microsoft.com/5e667044-1781-4380-b855-d15cf8cd2349">IVideoWindow::SetWindowPosition</a>
 

 

