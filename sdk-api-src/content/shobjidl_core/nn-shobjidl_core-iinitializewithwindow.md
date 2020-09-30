---
UID: NN:shobjidl_core.IInitializeWithWindow
title: IInitializeWithWindow (shobjidl_core.h)
description: Exposes a method through which a client can provide an owner window to a Windows Runtime object used in a desktop application.
helpviewer_keywords: ["IInitializeWithWindow","IInitializeWithWindow interface [Windows Shell]","IInitializeWithWindow interface [Windows Shell]","described","shell.IInitializeWithWindow","shobjidl_core/IInitializeWithWindow"]
old-location: shell\IInitializeWithWindow.htm
tech.root: shell
ms.assetid: 8421BFA0-0655-447c-99BB-3D4F049C572D
ms.date: 12/05/2018
ms.keywords: IInitializeWithWindow, IInitializeWithWindow interface [Windows Shell], IInitializeWithWindow interface [Windows Shell],described, shell.IInitializeWithWindow, shobjidl_core/IInitializeWithWindow
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IInitializeWithWindow
 - shobjidl_core/IInitializeWithWindow
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - IInitializeWithWindow
---

# IInitializeWithWindow interface


## -description

Exposes a method through which a client can provide an owner window to a Windows Runtime object used in a desktop application.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IInitializeWithWindow</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IInitializeWithWindow</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IInitializeWithWindow</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iinitializewithwindow-initialize">Initialize</a>
</td>
<td align="left" width="63%">
Specifies an owner window to be used by a Windows Runtime object that is used in a desktop app.

</td>
</tr>
</table>

## -remarks

<h3><a id="When_to_implement"></a><a id="when_to_implement"></a><a id="WHEN_TO_IMPLEMENT"></a>When to implement</h3>
Implement this interface if your object needs to be provided with an owner window, generally to display UI. Most third-party applications will not need to implement this interface.

<h3><a id="When_to_use"></a><a id="when_to_use"></a><a id="WHEN_TO_USE"></a>When to use</h3>
Use this interface if you will provide a window to an object. A common scenario in which this interface is used is a Windows Store desktop browser.

This interface is implemented by the following objects. Note that this is necessarily an incomplete list; refer to an individual object's documentation to determine whether that object implements this interface.

                

<ul>
<li><a href="/uwp/api/Windows.UI.Popups.PopupMenu">Windows.UI.Popups.PopupMenu</a></li>
<li><a href="/uwp/api/Windows.UI.Popups.MessageDialog">Windows.UI.Popups.MessageDialog</a></li>
<li><a href="/uwp/api/Windows.Storage.Pickers.FileOpenPicker">Windows.Storage.Pickers.FileOpenPicker</a></li>
<li><a href="/uwp/api/Windows.Storage.Pickers.FileSavePicker">Windows.Storage.Pickers.FileSavePicker</a></li>
<li><a href="/uwp/api/Windows.Storage.Pickers.FolderPicker">Windows.Storage.Pickers.FolderPicker</a></li>
<li><a href="/windows/desktop/shell/dataobject">CLSID_DragDropHelper</a></li>
</ul>