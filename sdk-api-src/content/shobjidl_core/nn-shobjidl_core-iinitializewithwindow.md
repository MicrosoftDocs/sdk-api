---
UID: NN:shobjidl_core.IInitializeWithWindow
title: IInitializeWithWindow
author: windows-sdk-content
description: Exposes a method through which a client can provide an owner window to a Windows Runtime object used in a desktop application.
old-location: shell\IInitializeWithWindow.htm
old-project: shell
ms.assetid: 8421BFA0-0655-447c-99BB-3D4F049C572D
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IInitializeWithWindow, IInitializeWithWindow interface [Windows Shell], IInitializeWithWindow interface [Windows Shell],described, shell.IInitializeWithWindow, shobjidl_core/IInitializeWithWindow
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.redist: 
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
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - IInitializeWithWindow
product: Windows
targetos: Windows
req.lib: Shell32.lib
req.dll: Shell32.dll (version 4.0 or later)
req.irql: 
req.product: Outlook Express 6.0
---

# IInitializeWithWindow interface


## -description


Exposes a method through which a client can provide an owner window to a Windows Runtime object used in a desktop application.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IInitializeWithWindow</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IInitializeWithWindow</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/429E5D12-9ED9-4f4f-A0E6-F95953C9113A">Initialize</a>
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
<li><a href="http://go.microsoft.com/fwlink/p/?linkid=267492">Windows.UI.Popups.PopupMenu</a></li>
<li><a href="http://go.microsoft.com/fwlink/p/?linkid=267493">Windows.UI.Popups.MessageDialog</a></li>
<li><a href="http://go.microsoft.com/fwlink/p/?linkid=267494">Windows.Storage.Pickers.FileOpenPicker</a></li>
<li><a href="http://go.microsoft.com/fwlink/p/?linkid=267495">Windows.Storage.Pickers.FileSavePicker</a></li>
<li><a href="http://go.microsoft.com/fwlink/p/?linkid=267496">Windows.Storage.Pickers.FolderPicker</a></li>
<li><a href="dataobject.htm">CLSID_DragDropHelper</a></li>
</ul>


