---
UID: NN:shlobj_core.IShellChangeNotify
title: IShellChangeNotify (shlobj_core.h)
description: Exposes a method that notifies a Shell namespace extension when the ID of an item has changed.
helpviewer_keywords: ["IShellChangeNotify","IShellChangeNotify interface [Windows Shell]","IShellChangeNotify interface [Windows Shell]","described","_win32_IShellChangeNotify","shell.IShellChangeNotify","shlobj_core/IShellChangeNotify"]
old-location: shell\IShellChangeNotify.htm
tech.root: shell
ms.assetid: fc8d0bdd-0ca5-40e3-bdad-68ca1c64b08e
ms.date: 12/05/2018
ms.keywords: IShellChangeNotify, IShellChangeNotify interface [Windows Shell], IShellChangeNotify interface [Windows Shell],described, _win32_IShellChangeNotify, shell.IShellChangeNotify, shlobj_core/IShellChangeNotify
req.header: shlobj_core.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - IShellChangeNotify
 - shlobj_core/IShellChangeNotify
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
 - IShellChangeNotify
---

# IShellChangeNotify interface


## -description

Exposes a method that notifies a Shell namespace extension when the ID of an item has changed.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IShellChangeNotify</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IShellChangeNotify</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IShellChangeNotify</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shlobj_core/nf-shlobj_core-ishellchangenotify-onchange">OnChange</a>
</td>
<td align="left" width="63%">
Informs a namespace extension that an event has taken place that affects its items.

</td>
</tr>
</table>

## -remarks

<b>IShellChangeNotify</b> is used to let a host of a component communicate the change notifications that it receives to the objects that it hosts. This is used in Windows Explorer to communicate change notifications to band objects.

This interface is implemented by all namespace extensions.

You do not call this interface directly. <b>IShellChangeNotify</b> is used by the operating system only when it has confirmed that your application is aware of this interface.

<b>IShellChangeNotify</b> implements <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> as well as the listed method.

