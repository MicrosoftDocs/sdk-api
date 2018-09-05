---
UID: NF:d3d9helper.IDirect3DStateBlock9.Capture
title: IDirect3DStateBlock9::Capture
author: windows-sdk-content
description: Capture the current value of states that are included in a stateblock.
old-location: direct3d9\idirect3dstateblock9__capture.htm
old-project: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3dstateblock9__capture.htm
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: 2f57837a-b161-c1f5-e5ba-7e4fda75185f, Capture, Capture method [Direct3D 9], Capture method [Direct3D 9],IDirect3DStateBlock9 interface, IDirect3DStateBlock9 interface [Direct3D 9],Capture method, IDirect3DStateBlock9.Capture, IDirect3DStateBlock9::Capture, d3d9helper/IDirect3DStateBlock9::Capture, direct3d9.idirect3dstateblock9__capture
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: d3d9helper.h
req.include-header: D3D9.h
req.redist: 
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
 - IDirect3DStateBlock9.Capture
product: Windows
targetos: Windows
req.lib: D3D9.lib
req.dll: 
req.irql: 
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
 

 

