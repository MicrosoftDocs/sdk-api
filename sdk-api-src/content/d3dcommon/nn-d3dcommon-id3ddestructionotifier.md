---
UID: NN:d3dcommon.ID3DDestructionNotifier
title: ID3DDestructionNotifier (d3dcommon.h)
description: ID3DDestructionNotifier is an include interface that the user implements to allow an application to call user-overridable methods for opening and closing shader
helpviewer_keywords: ["ID3DDestructionNotifier","ID3DDestructionNotifier interface [Direct3D]","ID3DDestructionNotifier interface [Direct3D]","described","d3dcommon/ID3DDestructionNotifier","direct3d.id3ddestructionnotifier"]
old-location: direct3d11\id3dinclude.htm
tech.root: direct3d11
ms.assetid: 2020ce65-3a6e-4a9f-9e97-b94e3c75f4f5
ms.date: 12/05/2018
ms.keywords: ID3DDestructionNotifier, ID3DDestructionNotifier interface [Direct3D], ID3DDestructionNotifier interface [Direct3D],described, d3dcommon/ID3DDestructionNotifier, direct3d.id3ddestructionnotifier
f1_keywords:
- d3dcommon/ID3DDestructionNotifier
dev_langs:
- c++
req.header: d3dcommon.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- D3DCommon.h
api_name:
- ID3DDestructionNotifier
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID3DInclude interface


## -description


<b>ID3DDestructionNotifier</b> is an interface that can be used to register for callbacks when a D3D Nano-COM object is destroyed.
To acquire an instance of this interface, call <a href="windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(refiid_void)"></a> on a D3D object with the **IID** of **ID3DDestructionNotifier**.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3DDestructionNotifier</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ID3DInclude</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID3DDestructionNotifier</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="windows/desktop/api/d3dcommon/nf-d3dcommon-id3ddestructionnotifier-registerdestructioncallback">RegisterDestructionCallback</a>
</td>
<td align="left" width="63%">
Registers a user-defined callback to be invoked when the current object is destroyed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="windows/desktop/api/d3dcommon/nf-d3dcommon-id3ddestructionnotifier-unregisterdestructioncallback">UnregisterDestructionCallback</a>
</td>
<td align="left" width="63%">
Unregisters a user-defined callback that was previously registered.

</td>
</tr>
</table> 


## -remarks

The <b>ID3DDestructionNotifier</b> can be used to track resources which are being unexpectedly released early, or providing a log of object disposal.


## -see-also

<a href="windows/desktop/api/d3dcommon/nf-d3dcommon-id3ddestructionnotifier-registerdestructioncallback">ID3DDestructionNotifier::RegisterDestructionCallback</a>



<a href="windows/desktop/api/d3dcommon/nf-d3dcommon-id3ddestructionnotifier-unregisterdestructioncallback">ID3DDestructionNotifier::UnregisterDestructionCallback</a>


<a href="https://docs.microsoft.com/windows/desktop/direct3d11/d3d11-graphics-reference-d3d11-common-interfaces">Common Version Interfaces</a>
 

 
