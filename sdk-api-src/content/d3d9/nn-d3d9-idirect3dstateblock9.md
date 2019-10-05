---
UID: NN:d3d9.IDirect3DStateBlock9
title: IDirect3DStateBlock9 (d3d9.h)
author: windows-sdk-content
description: Applications use the methods of the IDirect3DStateBlock9 interface to encapsulate render states.
old-location: direct3d9\idirect3dstateblock9.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3dstateblock9.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: 4d36b0db-f60c-4be1-3a29-4484c05de1bb, IDirect3DStateBlock9, IDirect3DStateBlock9 interface [Direct3D 9], IDirect3DStateBlock9 interface [Direct3D 9],described, d3d9helper/IDirect3DStateBlock9, direct3d9.idirect3dstateblock9
ms.topic: interface
f1_keywords: 
 - "d3d9/IDirect3DStateBlock9"
dev_langs:
 - c++
req.header: d3d9.h
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
req.lib: D3d9.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d3d9.lib
 - d3d9.dll
api_name:
 - IDirect3DStateBlock9
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDirect3DStateBlock9 interface


## -description


Applications use the methods of the IDirect3DStateBlock9 interface to encapsulate render states.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDirect3DStateBlock9</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDirect3DStateBlock9</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDirect3DStateBlock9</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3dstateblock9-apply">Apply</a>
</td>
<td align="left" width="63%">
Apply the state block to the current device state.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3dstateblock9-capture">Capture</a>
</td>
<td align="left" width="63%">
Capture the current value of states that are included in a stateblock.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3dstateblock9-getdevice">GetDevice</a>
</td>
<td align="left" width="63%">
Gets the device.

</td>
</tr>
</table> 


## -remarks



This interface can be used to save and restore pipeline state. It can also be used to capture the current state.

The LPDIRECT3DSTATEBLOCK9 and PDIRECT3DSTATEBLOCK9 types are defined as pointers to the <b>IDirect3DStateBlock9</b> interface.
    
            


```
typedef struct IDirect3DStateBlock9 *LPDIRECT3DSTATEBLOCK9, *PDIRECT3DSTATEBLOCK9;
```





## -see-also




<a href="https://docs.microsoft.com/windows/desktop/direct3d9/dx9-graphics-reference-d3d-interfaces">Direct3D Interfaces</a>
 

 

