---
UID: NN:shobjidl_core.IDeskBand
title: IDeskBand
author: windows-sdk-content
description: Used to obtain information about a band object.
old-location: shell\IDeskBand.htm
tech.root: shell
ms.assetid: eb9f7f2a-a6be-4527-8a32-325dad4c8000
ms.author: windowssdkdev
ms.date: 09/21/2018
ms.keywords: IDeskBand, IDeskBand interface [Windows Shell], IDeskBand interface [Windows Shell],described, _win32_IDeskBand, shell.IDeskBand, shobjidl_core/IDeskBand
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: shobjidl_core.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl_core.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Shell32.dll (version 4.71 or later)
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IDeskBand
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDeskBand interface


## -description


Used to obtain information about a band object.
<div class="alert"><b>Important</b>  You should use <a href="https://msdn.microsoft.com/cbf2b07d-d67c-4755-888c-d40692d13cae">thumbnail toolbars</a> in new development in place of desk bands, which are not supported as of Windows 7.</div><div> </div>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDeskBand</b> interface inherits from <a href="https://msdn.microsoft.com/9e80fd5e-f57d-4801-b198-73b8f5ffff6e">IDockingWindow</a>. <b>IDeskBand</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDeskBand</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7567a2f8-989e-4d11-ae55-209e4cfacad0">GetBandInfo</a>
</td>
<td align="left" width="63%">
Gets state information for a band object.

</td>
</tr>
</table> 


## -remarks



This interface also provides the methods of the <a href="https://msdn.microsoft.com/2d0efbae-4a1c-43b1-9021-8d89377f7282">IOleWindow</a> and <a href="https://msdn.microsoft.com/9e80fd5e-f57d-4801-b198-73b8f5ffff6e">IDockingWindow</a> interfaces, from which it inherits.

<h3><a id="When_to_Implement"></a><a id="when_to_implement"></a><a id="WHEN_TO_IMPLEMENT"></a>When to Implement</h3>
Implement <b>IDeskBand</b> if you are implementing a band object.

<h3><a id="When_to_Use"></a><a id="when_to_use"></a><a id="WHEN_TO_USE"></a>When to Use</h3>
You do not call this interface directly. <b>IDeskBand</b> is used by the Shell or the browser to obtain display information for a band object.




## -see-also




<a href="https://msdn.microsoft.com/4bf46b3f-f833-42e0-baf7-21bfa9e6d890">Creating Custom Explorer Bars, Tool Bands, and Desk Bands</a>



<a href="https://msdn.microsoft.com/9e80fd5e-f57d-4801-b198-73b8f5ffff6e">IDockingWindow</a>
 

 

