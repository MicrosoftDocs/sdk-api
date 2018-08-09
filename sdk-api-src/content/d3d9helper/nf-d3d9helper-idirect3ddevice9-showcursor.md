---
UID: NF:d3d9helper.IDirect3DDevice9.ShowCursor
title: IDirect3DDevice9::ShowCursor
author: windows-sdk-content
description: Displays or hides the cursor.
old-location: direct3d9\idirect3ddevice9__showcursor.htm
old-project: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9__showcursor.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IDirect3DDevice9 interface [Direct3D 9],ShowCursor method, IDirect3DDevice9.ShowCursor, IDirect3DDevice9::ShowCursor, ShowCursor, ShowCursor method [Direct3D 9], ShowCursor method [Direct3D 9],IDirect3DDevice9 interface, d3d9helper/IDirect3DDevice9::ShowCursor, direct3d9.idirect3ddevice9__showcursor, f4d45e5b-633f-a1a6-df58-ae9ec866fb60
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: d3d9helper.h
req.include-header: D3D9.h
req.target-type: Windows
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
tech.root: 
req.typenames: D3DVSHADERCAPS2_0
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D9.lib
 - D3D9.dll
api_name:
 - IDirect3DDevice9.ShowCursor
product: Windows
targetos: Windows
req.lib: D3D9.lib
req.dll: 
req.irql: 
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
Or users might want to call the <a href="https://msdn.microsoft.com/en-us/library/Bb174430(v=VS.85).aspx">IDirect3DDevice9::SetCursorProperties</a> method if they want to change the cursor. See the code in the DirectX Graphics C/C++ Samples for more detail.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb174336(v=VS.85).aspx">IDirect3DDevice9</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb174429(v=VS.85).aspx">IDirect3DDevice9::SetCursorPosition</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb174430(v=VS.85).aspx">IDirect3DDevice9::SetCursorProperties</a>
 

 

