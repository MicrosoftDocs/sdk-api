---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
<a href="https://msdn.microsoft.com/library/windows/hardware/ff550945">Initialize</a>
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


