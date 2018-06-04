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

# IDirect3DDevice9::ShowCursor


## -description


Displays or hides the cursor.


## -parameters




### -param bShow [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

If bShow is <b>TRUE</b>, the cursor is shown. If bShow is <b>FALSE</b>, the cursor is hidden. 


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

Value indicating whether the cursor was previously visible. <b>TRUE</b> if the cursor was previously visible, or <b>FALSE</b> if the cursor was not previously visible.




## -remarks



Direct3D cursor functions use either GDI cursor or software emulation, depending on the hardware. Users usually want to respond to a WM_SETCURSOR message. For example, the users might want to write the message handler like this:

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>
    
case WM_SETCURSOR:

// Turn off window cursor 
    
SetCursor( NULL );
    
m_pd3dDevice-&gt;ShowCursor( TRUE );
    
return TRUE; // prevent Windows from setting cursor to window class cursor
    
break;
</pre>
</td>
</tr>
</table></span></div>
Or users might want to call the <a href="https://msdn.microsoft.com/45e4935a-cdbd-4412-8ca5-fc4e1ceb6434">IDirect3DDevice9::SetCursorProperties</a> method if they want to change the cursor. See the code in the DirectX Graphics C/C++ Samples for more detail.




## -see-also




<a href="https://msdn.microsoft.com/cf951e8e-7adb-417a-bda0-9b3cde4912a7">IDirect3DDevice9</a>



<a href="https://msdn.microsoft.com/3b6410e5-fdeb-4390-b0c6-227f0c6666c6">IDirect3DDevice9::SetCursorPosition</a>



<a href="https://msdn.microsoft.com/45e4935a-cdbd-4412-8ca5-fc4e1ceb6434">IDirect3DDevice9::SetCursorProperties</a>
 

 

