---
UID: NN:dxgi1_6.IDXGIOutput6
title: IDXGIOutput6 (dxgi1_6.h)
author: windows-sdk-content
description: Represents an adapter output (such as a monitor). The IDXGIOutput6 interface exposes methods to provide specific monitor capabilities.
old-location: direct3ddxgi\idxgioutput6.htm
tech.root: direct3ddxgi
ms.assetid: 2F04E7F1-8295-441B-9E86-65C3DE5DE75F
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IDXGIOutput6, IDXGIOutput6 interface [DXGI], IDXGIOutput6 interface [DXGI],described, direct3ddxgi.idxgioutput6, dxgi1_6/IDXGIOutput6
ms.topic: interface
f1_keywords: ["dxgi1_6/IDXGIOutput6"]
req.header: dxgi1_6.h
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
 - IDXGIOutput6
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDXGIOutput6 interface


## -description


Represents an adapter output (such as a monitor). The <b>IDXGIOutput6</b> interface exposes  methods to provide specific monitor capabilities.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDXGIOutput6</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/dxgi1_5/nn-dxgi1_5-idxgioutput5">IDXGIOutput5</a>. <b>IDXGIOutput6</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDXGIOutput6</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dxgi1_6/nf-dxgi1_6-idxgioutput6-checkhardwarecompositionsupport">CheckHardwareCompositionSupport</a>
</td>
<td align="left" width="63%">
Notifies applications that hardware stretching is supported.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dxgi1_6/nf-dxgi1_6-idxgioutput6-getdesc1">GetDesc1</a>
</td>
<td align="left" width="63%">
Get an extended description of the output that includes color characteristics and connection type.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/direct3ddxgi/d3d10-graphics-reference-dxgi-interfaces">DXGI Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/api/dxgi1_5/nn-dxgi1_5-idxgioutput5">IDXGIOutput5</a>
 

 

