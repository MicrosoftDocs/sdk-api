---
UID: NN:dxgi1_2.IDXGIOutput1
title: IDXGIOutput1 (dxgi1_2.h)
author: windows-sdk-content
description: An IDXGIOutput1 interface represents an adapter output (such as a monitor).
old-location: direct3ddxgi\idxgioutput1.htm
tech.root: direct3ddxgi
ms.assetid: 27C7BD34-0746-4D5F-A746-45FFEE5BCD31
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IDXGIOutput1, IDXGIOutput1 interface [DXGI], IDXGIOutput1 interface [DXGI],described, direct3ddxgi.idxgioutput1, dxgi1_2/IDXGIOutput1
ms.topic: interface
f1_keywords: 
 - "dxgi1_2/IDXGIOutput1"
dev_langs:
 - c++
req.header: dxgi1_2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 and Platform Update for Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 and Platform Update for Windows Server 2008 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: DXGI.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - DXGI.lib
 - DXGI.dll
api_name:
 - IDXGIOutput1
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDXGIOutput1 interface


## -description


An <b>IDXGIOutput1</b> interface represents an adapter output (such as a monitor).


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDXGIOutput1</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/dxgi/nn-dxgi-idxgioutput">IDXGIOutput</a>. <b>IDXGIOutput1</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDXGIOutput1</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgioutput1-duplicateoutput">DuplicateOutput</a>
</td>
<td align="left" width="63%">
Creates a desktop duplication interface from the <b>IDXGIOutput1</b> interface that represents an adapter output.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgioutput1-findclosestmatchingmode1">FindClosestMatchingMode1</a>
</td>
<td align="left" width="63%">
Finds the display mode that most closely matches the requested display mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgioutput1-getdisplaymodelist1">GetDisplayModeList1</a>
</td>
<td align="left" width="63%">
Gets the display modes that match the requested format and other input options.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgioutput1-getdisplaysurfacedata1">GetDisplaySurfaceData1</a>
</td>
<td align="left" width="63%">
Copies the display surface (front buffer) to a user-provided resource.

</td>
</tr>
</table> 


## -remarks



To determine  the outputs that are available from the adapter, use <a href="https://docs.microsoft.com/windows/desktop/api/dxgi/nf-dxgi-idxgiadapter-enumoutputs">IDXGIAdapter::EnumOutputs</a>. To determine the specific output that the swap chain will update, use <a href="https://docs.microsoft.com/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-getcontainingoutput">IDXGISwapChain::GetContainingOutput</a>. You can then call <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q_)">QueryInterface</a> from any  <a href="https://docs.microsoft.com/windows/desktop/api/dxgi/nn-dxgi-idxgioutput">IDXGIOutput</a> object to obtain an <b>IDXGIOutput1</b> object.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/direct3ddxgi/d3d10-graphics-reference-dxgi-interfaces">DXGI Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/api/dxgi/nn-dxgi-idxgioutput">IDXGIOutput</a>
 

 

