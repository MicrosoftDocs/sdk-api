---
UID: NN:shobjidl.IDeskBand2
title: IDeskBand2 (shobjidl.h)
description: Exposes methods to enable and query translucency effects in a deskband object.
helpviewer_keywords: ["IDeskBand2","IDeskBand2 interface [Windows Shell]","IDeskBand2 interface [Windows Shell]","described","_shell_IDeskBand2","shell.IDeskBand2","shobjidl/IDeskBand2"]
old-location: shell\IDeskBand2.htm
tech.root: shell
ms.assetid: ba73527a-7762-45c0-8c69-87f03e55e5c6
ms.date: 12/05/2018
ms.keywords: IDeskBand2, IDeskBand2 interface [Windows Shell], IDeskBand2 interface [Windows Shell],described, _shell_IDeskBand2, shell.IDeskBand2, shobjidl/IDeskBand2
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDeskBand2
 - shobjidl/IDeskBand2
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IDeskBand2
---

# IDeskBand2 interface


## -description

Exposes methods to enable and query translucency effects in a deskband object.
<div class="alert"><b>Important</b>  You should use <a href="/windows/desktop/shell/taskbar-extensions">thumbnail toolbars</a> in new development in place of desk bands, which are not supported as of Windows 7.</div><div> </div>

## -inheritance

The <b>IDeskBand2</b> interface inherits from <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ideskband">IDeskBand</a>. <b>IDeskBand2</b> also has these types of members:

## -remarks

This interface also provides the methods of the <a href="/windows/desktop/api/oleidl/nn-oleidl-iolewindow">IOleWindow</a>, <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idockingwindow">IDockingWindow</a>, and <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ideskband">IDeskBand</a> interfaces, from which it inherits.

If implemented in all active deskbands, this interface allows the taskbar to be displayed using translucent effects. If an active deskband does not implement <b>IDeskBand2</b>, then translucency is disabled for the entire taskbar.

A deskband can implement <b>IDeskBand2</b> as a communication conduit between itself and the taskbar as follows:

                

<ul>
<li>Taskbar calls <a href="/windows/desktop/api/shobjidl/nf-shobjidl-ideskband2-canrendercomposited">IDeskBand2::CanRenderComposited</a> to learn if a deskband supports translucency. If one or more do not, the entire taskbar is rendered opaque.</li>
<li>Taskbar calls <a href="/windows/desktop/api/shobjidl/nf-shobjidl-ideskband2-setcompositionstate">IDeskBand2::SetCompositionState</a> as appropriate in response to a user turning translucent effects on or off. The taskbar should attempt to render itself translucent or opaque in response to this call.</li>
<li>
<a href="/windows/desktop/api/shobjidl/nf-shobjidl-ideskband2-getcompositionstate">IDeskBand2::GetCompositionState</a> is the counterpart of <a href="/windows/desktop/api/shobjidl/nf-shobjidl-ideskband2-setcompositionstate">IDeskBand2::SetCompositionState</a>.</li>
</ul>
