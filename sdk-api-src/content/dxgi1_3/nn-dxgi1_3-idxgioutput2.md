---
UID: NN:dxgi1_3.IDXGIOutput2
title: IDXGIOutput2
author: windows-sdk-content
description: Represents an adapter output (such as a monitor). The IDXGIOutput2 interface exposes a method to check for multiplane overlay support on the primary output adapter.
old-location: direct3ddxgi\idxgioutput2.htm
old-project: direct3ddxgi
ms.assetid: 23585A1F-3F18-4247-91DB-712C0A8D5398
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: IDXGIOutput2, IDXGIOutput2 interface [DXGI], IDXGIOutput2 interface [DXGI],described, direct3ddxgi.idxgioutput2, dxgi1_3/IDXGIOutput2
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: dxgi1_3.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps | UWP apps]
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
req.typenames: DXGI_OVERLAY_SUPPORT_FLAG
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - DXGI.lib
 - DXGI.dll
api_name:
 - IDXGIOutput2
product: Windows
targetos: Windows
req.lib: DXGI.lib
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDXGIOutput2 interface


## -description


Represents an adapter output (such as a monitor). The <b>IDXGIOutput2</b> interface exposes a method to check for multiplane overlay support on the primary output adapter.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDXGIOutput2</b> interface inherits from <a href="https://msdn.microsoft.com/27C7BD34-0746-4D5F-A746-45FFEE5BCD31">IDXGIOutput1</a>. <b>IDXGIOutput2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDXGIOutput2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/BC9CD287-CD89-4D0C-ADE3-EAA60D5FEAAD">SupportsOverlays</a>
</td>
<td align="left" width="63%">
Queries an adapter output for multiplane overlay support.

</td>
</tr>
</table> 


## -remarks



To determine  the outputs that are available from the adapter, use <a href="https://msdn.microsoft.com/29a826bb-6282-41d1-abf9-642ccb127774">IDXGIAdapter::EnumOutputs</a>. To determine the specific output that the swap chain will update, use <a href="https://msdn.microsoft.com/0ebc1ec3-87f3-46bc-8516-180d28740b38">IDXGISwapChain::GetContainingOutput</a>. You can then call <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">QueryInterface</a> from any  <a href="https://msdn.microsoft.com/c641995e-a4d9-4bfb-bdc0-7ffbe77c3599">IDXGIOutput</a> or <a href="https://msdn.microsoft.com/27C7BD34-0746-4D5F-A746-45FFEE5BCD31">IDXGIOutput1</a> object to obtain an <b>IDXGIOutput2</b> object.




## -see-also




<a href="https://msdn.microsoft.com/b561b26b-961c-4d5e-8483-56b51b989bf7">DXGI Interfaces</a>



<a href="https://msdn.microsoft.com/27C7BD34-0746-4D5F-A746-45FFEE5BCD31">IDXGIOutput1</a>
 

 

