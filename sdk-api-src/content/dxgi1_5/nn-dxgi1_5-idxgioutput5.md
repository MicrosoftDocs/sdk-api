---
UID: NN:dxgi1_5.IDXGIOutput5
title: IDXGIOutput5 (dxgi1_5.h)
description: Represents an adapter output (such as a monitor). The IDXGIOutput5 interface exposes a single method to specify a list of supported formats for fullscreen surfaces.
helpviewer_keywords: ["IDXGIOutput5","IDXGIOutput5 interface [DXGI]","IDXGIOutput5 interface [DXGI]","described","direct3ddxgi.idxgioutput5","dxgi1_5/IDXGIOutput5"]
old-location: direct3ddxgi\idxgioutput5.htm
tech.root: direct3ddxgi
ms.assetid: D75529BD-C572-4137-8F1E-91F7C6902EE0
ms.date: 12/05/2018
ms.keywords: IDXGIOutput5, IDXGIOutput5 interface [DXGI], IDXGIOutput5 interface [DXGI],described, direct3ddxgi.idxgioutput5, dxgi1_5/IDXGIOutput5
f1_keywords:
- dxgi1_5/IDXGIOutput5
dev_langs:
- c++
req.header: dxgi1_5.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Dxgi.lib
req.dll: Dxgi.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- dxgi.dll
api_name:
- IDXGIOutput5
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDXGIOutput5 interface


## -description


Represents an adapter output (such as a monitor). The <b>IDXGIOutput5</b> interface exposes a single method to specify a list of supported formats for fullscreen surfaces.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDXGIOutput5</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/dxgi1_4/nn-dxgi1_4-idxgioutput4">IDXGIOutput4</a>. <b>IDXGIOutput5</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDXGIOutput5</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dxgi1_5/nf-dxgi1_5-idxgioutput5-duplicateoutput1">DuplicateOutput1</a>
</td>
<td align="left" width="63%">
Allows specifying a list of supported formats for fullscreen surfaces that can be returned by the <a href="https://docs.microsoft.com/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgioutputduplication">IDXGIOutputDuplication</a> object.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/direct3ddxgi/d3d10-graphics-reference-dxgi-interfaces">DXGI Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/api/dxgi1_4/nn-dxgi1_4-idxgioutput4">IDXGIOutput4</a>
 

 

