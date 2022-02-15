---
UID: NN:shobjidl_core.IDeskBand
title: IDeskBand (shobjidl_core.h)
description: Used to obtain information about a band object.
helpviewer_keywords: ["IDeskBand","IDeskBand interface [Windows Shell]","IDeskBand interface [Windows Shell]","described","_win32_IDeskBand","shell.IDeskBand","shobjidl_core/IDeskBand"]
old-location: shell\IDeskBand.htm
tech.root: shell
ms.assetid: eb9f7f2a-a6be-4527-8a32-325dad4c8000
ms.date: 12/05/2018
ms.keywords: IDeskBand, IDeskBand interface [Windows Shell], IDeskBand interface [Windows Shell],described, _win32_IDeskBand, shell.IDeskBand, shobjidl_core/IDeskBand
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDeskBand
 - shobjidl_core/IDeskBand
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
 - IDeskBand
---

# IDeskBand interface


## -description

Used to obtain information about a band object.
<div class="alert"><b>Important</b>  You should use <a href="/windows/desktop/shell/taskbar-extensions">thumbnail toolbars</a> in new development in place of desk bands, which are not supported as of Windows 7.</div><div> </div>

## -inheritance

The <b>IDeskBand</b> interface inherits from <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idockingwindow">IDockingWindow</a>. <b>IDeskBand</b> also has these types of members:

## -remarks

This interface also provides the methods of the <a href="/windows/desktop/api/oleidl/nn-oleidl-iolewindow">IOleWindow</a> and <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idockingwindow">IDockingWindow</a> interfaces, from which it inherits.

<h3><a id="When_to_Implement"></a><a id="when_to_implement"></a><a id="WHEN_TO_IMPLEMENT"></a>When to Implement</h3>
Implement <b>IDeskBand</b> if you are implementing a band object.

<h3><a id="When_to_Use"></a><a id="when_to_use"></a><a id="WHEN_TO_USE"></a>When to Use</h3>
You do not call this interface directly. <b>IDeskBand</b> is used by the Shell or the browser to obtain display information for a band object.

## -see-also

<a href="/previous-versions/windows/desktop/legacy/cc144099(v=vs.85)">Creating Custom Explorer Bars, Tool Bands, and Desk Bands</a>



<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idockingwindow">IDockingWindow</a>
