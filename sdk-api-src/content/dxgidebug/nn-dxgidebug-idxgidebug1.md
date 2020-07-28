---
UID: NN:dxgidebug.IDXGIDebug1
title: IDXGIDebug1 (dxgidebug.h)
description: Controls debug settings for Microsoft DirectX Graphics Infrastructure (DXGI). You can use the IDXGIDebug1 interface in Windows Store apps.
helpviewer_keywords: ["IDXGIDebug1","IDXGIDebug1 interface [DXGI]","IDXGIDebug1 interface [DXGI]","described","direct3ddxgi.idxgidebug1","dxgidebug/IDXGIDebug1"]
old-location: direct3ddxgi\idxgidebug1.htm
tech.root: direct3ddxgi
ms.assetid: 16D52CA2-1495-407C-9B88-CF4D4C90BAFA
ms.date: 12/05/2018
ms.keywords: IDXGIDebug1, IDXGIDebug1 interface [DXGI], IDXGIDebug1 interface [DXGI],described, direct3ddxgi.idxgidebug1, dxgidebug/IDXGIDebug1
f1_keywords:
- dxgidebug/IDXGIDebug1
dev_langs:
- c++
req.header: dxgidebug.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: DXGIDebug.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- DXGIDebug.dll
api_name:
- IDXGIDebug1
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDXGIDebug1 interface


## -description


Controls debug settings for Microsoft DirectX Graphics Infrastructure (DXGI). You can use the  <b>IDXGIDebug1</b> interface in Windows Store apps. 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDXGIDebug1</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/dxgidebug/nn-dxgidebug-idxgidebug">IDXGIDebug</a>. <b>IDXGIDebug1</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDXGIDebug1</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dxgidebug/nf-dxgidebug-idxgidebug1-disableleaktrackingforthread">DisableLeakTrackingForThread</a>
</td>
<td align="left" width="63%">
Stops tracking leaks for the current thread.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dxgidebug/nf-dxgidebug-idxgidebug1-enableleaktrackingforthread">EnableLeakTrackingForThread</a>
</td>
<td align="left" width="63%">
Starts tracking leaks for the current thread.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dxgidebug/nf-dxgidebug-idxgidebug1-isleaktrackingenabledforthread">IsLeakTrackingEnabledForThread</a>
</td>
<td align="left" width="63%">
Gets a value indicating whether leak tracking is turned on for the current thread.

</td>
</tr>
</table> 


## -remarks



Call the <a href="https://docs.microsoft.com/windows/desktop/api/dxgi1_3/nf-dxgi1_3-dxgigetdebuginterface1">DXGIGetDebugInterface1</a> function to obtain the <b>IDXGIDebug1</b> interface.

The <b>IDXGIDebug1</b> interface can be used only if the debug layer is turned on. For more info, see <a href="https://docs.microsoft.com/windows/desktop/direct3d11/overviews-direct3d-11-devices-layers">Debug Layer</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/direct3ddxgi/d3d10-graphics-reference-dxgi-interfaces">DXGI Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/api/dxgi1_3/nf-dxgi1_3-dxgigetdebuginterface1">DXGIGetDebugInterface1</a>



<a href="https://docs.microsoft.com/windows/desktop/api/dxgidebug/nn-dxgidebug-idxgidebug">IDXGIDebug</a>
 

 

