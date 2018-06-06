---
UID: NN:dxgi1_5.IDXGIOutput5
title: IDXGIOutput5
author: windows-sdk-content
description: Represents an adapter output (such as a monitor). The IDXGIOutput5 interface exposes a single method to specify a list of supported formats for fullscreen surfaces.
old-location: direct3ddxgi\idxgioutput5.htm
old-project: direct3ddxgi
ms.assetid: D75529BD-C572-4137-8F1E-91F7C6902EE0
ms.author: windowssdkdev
ms.date: 05/17/2018
ms.keywords: IDXGIOutput5, IDXGIOutput5 interface [DXGI], IDXGIOutput5 interface [DXGI],described, direct3ddxgi.idxgioutput5, dxgi1_5/IDXGIOutput5
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
tech.root: 
req.typenames: DXGI_RECLAIM_RESOURCE_RESULTS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dxgi.dll
api_name:
 - IDXGIOutput5
product: Windows
targetos: Windows
req.lib: Dxgi.lib
req.dll: Dxgi.dll
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDXGIOutput5 interface


## -description


Represents an adapter output (such as a monitor). The <b>IDXGIOutput5</b> interface exposes a single method to specify a list of supported formats for fullscreen surfaces.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDXGIOutput5</b> interface inherits from <a href="https://msdn.microsoft.com/6B9B4242-7B10-4022-9105-6903FEAE1161">IDXGIOutput4</a>. <b>IDXGIOutput5</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/B6723F05-E0D9-4814-8AB8-796ECF9C5C0C">DuplicateOutput1</a>
</td>
<td align="left" width="63%">
Allows specifying a list of supported formats for fullscreen surfaces that can be returned by the <a href="https://msdn.microsoft.com/02C4EC3D-D97F-4CFC-ABF5-03B44CE6A658">IDXGIOutputDuplication</a> object.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/b561b26b-961c-4d5e-8483-56b51b989bf7">DXGI Interfaces</a>



<a href="https://msdn.microsoft.com/6B9B4242-7B10-4022-9105-6903FEAE1161">IDXGIOutput4</a>
 

 

