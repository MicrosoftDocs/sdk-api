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

# IDirect3D9::GetAdapterMonitor


## -description


Returns the handle of the monitor associated with the Direct3D object.


## -parameters




### -param Adapter [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Ordinal number that denotes the display adapter. D3DADAPTER_DEFAULT is always the primary display adapter. 


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HMONITOR</a></b>

Handle of the monitor associated with the Direct3D object.




## -remarks



As shown in the following code fragment, which illustrates how to obtain a handle to the monitor associated with a given device, use <a href="https://msdn.microsoft.com/42666561-fb2b-47b4-b2c4-49926ea67964">GetDirect3D</a> to return the Direct3D enumerator from the device and use <a href="https://msdn.microsoft.com/18889d40-a64f-41da-92dd-7b197749e685">GetCreationParameters</a> to retrieve the value for Adapter.

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>
    if( FAILED( pDevice-&gt;GetCreationParameters(  &amp;Parameters ) ) )
        return D3DERR_INVALIDCALL;
    
    if( FAILED( pDevice-&gt;GetDirect3D(&amp;pD3D) ) )
        return D3DERR_INVALIDCALL;
    
    hMonitor = pD3D-&gt;GetAdapterMonitor(Parameters.AdapterOrdinal);
    
    pD3D-&gt;Release();
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/18889d40-a64f-41da-92dd-7b197749e685">GetCreationParameters</a>



<a href="https://msdn.microsoft.com/42666561-fb2b-47b4-b2c4-49926ea67964">GetDirect3D</a>



<a href="https://msdn.microsoft.com/af321e4f-aaff-4285-bdac-9aab5c1dc5d8">IDirect3D9</a>
 

 

