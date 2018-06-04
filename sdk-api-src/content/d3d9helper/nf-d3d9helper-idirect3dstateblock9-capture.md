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

# IDirect3DStateBlock9::Capture


## -description


Capture the current value of states that are included in a stateblock.


## -parameters






## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails because capture cannot be done while in record mode, the return value is D3DERR_INVALIDCALL.




## -remarks



The Capture method captures current values for states within an existing state block. It does not capture the entire state of the device. For example:

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>
IDirect3DStateBlock9* pStateBlock = NULL;

pd3dDevice-&gt;BeginStateBlock();
// Add the ZENABLE state to the stateblock 
pd3dDevice-&gt;SetRenderState ( D3DRS_ZENABLE, D3DZB_TRUE );
pd3dDevice-&gt;EndStateBlock ( &amp;pStateBlock );
    
// Change the current value that is stored in the state block
pd3dDevice-&gt;SetRenderState ( D3DRS_ZENABLE, D3DZB_FALSE );
pStateBlock-&gt;Capture();			

pStateBlock-&gt;Release();
</pre>
</td>
</tr>
</table></span></div>
Creating an empty stateblock and calling the Capture method does nothing if no states have been set.

The Capture method  will not capture information for lights that are explicitly or implicitly created after the stateblock is created.




## -see-also




<a href="https://msdn.microsoft.com/bb0dfea8-14ba-4d9d-acb7-9748258e0f35">IDirect3DStateBlock9</a>
 

 

