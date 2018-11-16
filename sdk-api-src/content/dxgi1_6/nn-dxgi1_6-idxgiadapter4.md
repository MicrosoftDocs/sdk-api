---
UID: NN:dxgi1_6.IDXGIAdapter4
title: IDXGIAdapter4
author: windows-sdk-content
description: This interface represents a display subsystem, and extends this family of interfaces to expose a method to check for an adapter's compatibility with Arbitrary Code Guard (ACG).
old-location: direct3ddxgi\idxgiadapter4.htm
tech.root: direct3ddxgi
ms.assetid: 176958F9-94C8-4F80-B9A4-96BC9634292E
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IDXGIAdapter4, IDXGIAdapter4 interface [DXGI], IDXGIAdapter4 interface [DXGI],described, direct3ddxgi.idxgiadapter4, dxgi1_6/IDXGIAdapter4
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: dxgi1_6.h
req.include-header: 
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
 - IDXGIAdapter4
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDXGIAdapter4 interface


## -description


This interface represents a display subsystem, and extends this family of interfaces to expose a method to check for an adapter's compatibility with Arbitrary Code Guard (ACG).


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDXGIAdapter4</b> interface inherits from <a href="https://msdn.microsoft.com/547840B4-4AAB-4049-8D79-BD34BA4D32CD">IDXGIAdapter3</a>. <b>IDXGIAdapter4</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDXGIAdapter4</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2C6C215C-8CD6-4650-A851-B82068E0F252">GetDesc3</a>
</td>
<td align="left" width="63%">
Gets a DXGI 1.6 description of an adapter or video card. This description includes information about ACG compatibility.

</td>
</tr>
</table> 


## -remarks



For more details, refer to the <a href="https://msdn.microsoft.com/956F80D7-EEC8-4D88-B251-EE325614F31E">Residency</a> section of the D3D12 documentation.




## -see-also




<a href="https://msdn.microsoft.com/b561b26b-961c-4d5e-8483-56b51b989bf7">DXGI Interfaces</a>



<a href="https://msdn.microsoft.com/547840B4-4AAB-4049-8D79-BD34BA4D32CD">IDXGIAdapter3</a>
 

 

