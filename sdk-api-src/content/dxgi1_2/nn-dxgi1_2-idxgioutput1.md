---
UID: NN:dxgi1_2.IDXGIOutput1
title: IDXGIOutput1
author: windows-sdk-content
description: An IDXGIOutput1 interface represents an adapter output (such as a monitor).
old-location: direct3ddxgi\idxgioutput1.htm
tech.root: direct3ddxgi
ms.assetid: 27C7BD34-0746-4D5F-A746-45FFEE5BCD31
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IDXGIOutput1, IDXGIOutput1 interface [DXGI], IDXGIOutput1 interface [DXGI],described, direct3ddxgi.idxgioutput1, dxgi1_2/IDXGIOutput1
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDXGIOutput1 interface


## -description


An <b>IDXGIOutput1</b> interface represents an adapter output (such as a monitor).


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDXGIOutput1</b> interface inherits from <a href="https://msdn.microsoft.com/en-us/library/Bb174546(v=VS.85).aspx">IDXGIOutput</a>. <b>IDXGIOutput1</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/32B13906-0920-4891-B1E7-BCB291E78E73">DuplicateOutput</a>
</td>
<td align="left" width="63%">
Creates a desktop duplication interface from the <b>IDXGIOutput1</b> interface that represents an adapter output.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/D71ED536-0D90-4E0D-8683-6260E31EAF20">FindClosestMatchingMode1</a>
</td>
<td align="left" width="63%">
Finds the display mode that most closely matches the requested display mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/49522ED9-30AD-4F39-96D2-BB6677D72349">GetDisplayModeList1</a>
</td>
<td align="left" width="63%">
Gets the display modes that match the requested format and other input options.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/120BC7CD-A4B2-4688-9A11-0BD59761B5F1">GetDisplaySurfaceData1</a>
</td>
<td align="left" width="63%">
Copies the display surface (front buffer) to a user-provided resource.

</td>
</tr>
</table> 


## -remarks



To determine  the outputs that are available from the adapter, use <a href="https://msdn.microsoft.com/en-us/library/Bb174525(v=VS.85).aspx">IDXGIAdapter::EnumOutputs</a>. To determine the specific output that the swap chain will update, use <a href="https://msdn.microsoft.com/en-us/library/Bb174571(v=VS.85).aspx">IDXGISwapChain::GetContainingOutput</a>. You can then call <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">QueryInterface</a> from any  <a href="https://msdn.microsoft.com/en-us/library/Bb174546(v=VS.85).aspx">IDXGIOutput</a> object to obtain an <b>IDXGIOutput1</b> object.




## -see-also




<a href="https://msdn.microsoft.com/b561b26b-961c-4d5e-8483-56b51b989bf7">DXGI Interfaces</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb174546(v=VS.85).aspx">IDXGIOutput</a>
 

 

