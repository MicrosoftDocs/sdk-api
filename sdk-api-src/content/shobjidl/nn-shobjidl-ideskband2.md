---
UID: NN:shobjidl.IDeskBand2
title: IDeskBand2
author: windows-sdk-content
description: Exposes methods to enable and query translucency effects in a deskband object.
old-location: shell\IDeskBand2.htm
old-project: shell
ms.assetid: ba73527a-7762-45c0-8c69-87f03e55e5c6
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: IDeskBand2, IDeskBand2 interface [Windows Shell], IDeskBand2 interface [Windows Shell],described, _shell_IDeskBand2, shell.IDeskBand2, shobjidl/IDeskBand2
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: shobjidl.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: VPWATERMARKFLAGS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IDeskBand2
product: Windows
targetos: Windows
req.lib: Shell32.lib
req.dll: Shell32.dll
req.irql: 
req.product: Internet Explorer 6.01
---

# IDeskBand2 interface


## -description


Exposes methods to enable and query translucency effects in a deskband object.
<div class="alert"><b>Important</b>  You should use <a href="https://msdn.microsoft.com/cbf2b07d-d67c-4755-888c-d40692d13cae">thumbnail toolbars</a> in new development in place of desk bands, which are not supported as of Windows 7.</div><div> </div>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDeskBand2</b> interface inherits from <a href="https://msdn.microsoft.com/eb9f7f2a-a6be-4527-8a32-325dad4c8000">IDeskBand</a>. <b>IDeskBand2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDeskBand2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/af42c03f-04aa-42b2-9be4-b3bfa0a8c47e">CanRenderComposited</a>
</td>
<td align="left" width="63%">
Indicates the deskband's ability to be displayed as translucent.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/77c9203b-39a1-4923-a5df-68861e19e9f1">GetCompositionState</a>
</td>
<td align="left" width="63%">
Gets the composition state.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/183cc6fa-4dc4-4272-8d61-a0a426aeefda">SetCompositionState</a>
</td>
<td align="left" width="63%">
Sets the composition state.

</td>
</tr>
</table> 


## -remarks



This interface also provides the methods of the <a href="https://msdn.microsoft.com/2d0efbae-4a1c-43b1-9021-8d89377f7282">IOleWindow</a>, <a href="https://msdn.microsoft.com/9e80fd5e-f57d-4801-b198-73b8f5ffff6e">IDockingWindow</a>, and <a href="https://msdn.microsoft.com/eb9f7f2a-a6be-4527-8a32-325dad4c8000">IDeskBand</a> interfaces, from which it inherits.

If implemented in all active deskbands, this interface allows the taskbar to be displayed using translucent effects. If an active deskband does not implement <b>IDeskBand2</b>, then translucency is disabled for the entire taskbar.

A deskband can implement <b>IDeskBand2</b> as a communication conduit between itself and the taskbar as follows:

                

<ul>
<li>Taskbar calls <a href="https://msdn.microsoft.com/af42c03f-04aa-42b2-9be4-b3bfa0a8c47e">IDeskBand2::CanRenderComposited</a> to learn if a deskband supports translucency. If one or more do not, the entire taskbar is rendered opaque.</li>
<li>Taskbar calls <a href="https://msdn.microsoft.com/183cc6fa-4dc4-4272-8d61-a0a426aeefda">IDeskBand2::SetCompositionState</a> as appropriate in response to a user turning translucent effects on or off. The taskbar should attempt to render itself translucent or opaque in response to this call.</li>
<li>
<a href="https://msdn.microsoft.com/77c9203b-39a1-4923-a5df-68861e19e9f1">IDeskBand2::GetCompositionState</a> is the counterpart of <a href="https://msdn.microsoft.com/183cc6fa-4dc4-4272-8d61-a0a426aeefda">IDeskBand2::SetCompositionState</a>.</li>
</ul>


