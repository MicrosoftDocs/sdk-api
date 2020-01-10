---
UID: NN:shobjidl.IDeskBand2
title: IDeskBand2 (shobjidl.h)
description: Exposes methods to enable and query translucency effects in a deskband object.
old-location: shell\IDeskBand2.htm
tech.root: shell
ms.assetid: ba73527a-7762-45c0-8c69-87f03e55e5c6
ms.date: 12/05/2018
ms.keywords: IDeskBand2, IDeskBand2 interface [Windows Shell], IDeskBand2 interface [Windows Shell],described, _shell_IDeskBand2, shell.IDeskBand2, shobjidl/IDeskBand2
f1_keywords:
- shobjidl/IDeskBand2
dev_langs:
- c++
req.header: shobjidl.h
req.include-header: 
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
req.lib: 
req.dll: Shell32.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Shell32.dll
api_name:
- IDeskBand2
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDeskBand2 interface


## -description


Exposes methods to enable and query translucency effects in a deskband object.
<div class="alert"><b>Important</b>  You should use <a href="https://docs.microsoft.com/windows/desktop/shell/taskbar-extensions">thumbnail toolbars</a> in new development in place of desk bands, which are not supported as of Windows 7.</div><div> </div>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDeskBand2</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ideskband">IDeskBand</a>. <b>IDeskBand2</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl/nf-shobjidl-ideskband2-canrendercomposited">CanRenderComposited</a>
</td>
<td align="left" width="63%">
Indicates the deskband's ability to be displayed as translucent.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl/nf-shobjidl-ideskband2-getcompositionstate">GetCompositionState</a>
</td>
<td align="left" width="63%">
Gets the composition state.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl/nf-shobjidl-ideskband2-setcompositionstate">SetCompositionState</a>
</td>
<td align="left" width="63%">
Sets the composition state.

</td>
</tr>
</table> 


## -remarks



This interface also provides the methods of the <a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nn-oleidl-iolewindow">IOleWindow</a>, <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idockingwindow">IDockingWindow</a>, and <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ideskband">IDeskBand</a> interfaces, from which it inherits.

If implemented in all active deskbands, this interface allows the taskbar to be displayed using translucent effects. If an active deskband does not implement <b>IDeskBand2</b>, then translucency is disabled for the entire taskbar.

A deskband can implement <b>IDeskBand2</b> as a communication conduit between itself and the taskbar as follows:

                

<ul>
<li>Taskbar calls <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl/nf-shobjidl-ideskband2-canrendercomposited">IDeskBand2::CanRenderComposited</a> to learn if a deskband supports translucency. If one or more do not, the entire taskbar is rendered opaque.</li>
<li>Taskbar calls <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl/nf-shobjidl-ideskband2-setcompositionstate">IDeskBand2::SetCompositionState</a> as appropriate in response to a user turning translucent effects on or off. The taskbar should attempt to render itself translucent or opaque in response to this call.</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl/nf-shobjidl-ideskband2-getcompositionstate">IDeskBand2::GetCompositionState</a> is the counterpart of <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl/nf-shobjidl-ideskband2-setcompositionstate">IDeskBand2::SetCompositionState</a>.</li>
</ul>


