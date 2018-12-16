---
UID: NN:shobjidl_core.ICommDlgBrowser2
title: ICommDlgBrowser2
author: windows-sdk-content
description: Extends the capabilities of ICommDlgBrowser. This interface is exposed by the common file dialog boxes when they host a Shell browser. A pointer to ICommDlgBrowser2 can be obtained by calling QueryInterface on the IShellBrowser object.
old-location: shell\ICommDlgBrowser2.htm
tech.root: shell
ms.assetid: 07a416a2-340d-4308-a6f3-cf6f19f3c906
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ICommDlgBrowser2, ICommDlgBrowser2 interface [Windows Shell], ICommDlgBrowser2 interface [Windows Shell],described, _win32_ICommDlgBrowser2, shell.ICommDlgBrowser2, shobjidl_core/ICommDlgBrowser2
ms.topic: interface
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - ICommDlgBrowser2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICommDlgBrowser2 interface


## -description


Extends the capabilities of <a href="https://msdn.microsoft.com/bf89ac6e-6c2e-4944-885c-9ab62f58fe71">ICommDlgBrowser</a>. This interface is exposed by the common file dialog boxes when they host a Shell browser. A pointer to <b>ICommDlgBrowser2</b> can be obtained by calling <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">QueryInterface</a> on the <a href="https://msdn.microsoft.com/138d90e3-a1f0-4faf-88ca-16c7a46df0ca">IShellBrowser</a> object.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICommDlgBrowser2</b> interface inherits from <a href="https://msdn.microsoft.com/bf89ac6e-6c2e-4944-885c-9ab62f58fe71">ICommDlgBrowser</a>. <b>ICommDlgBrowser2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ICommDlgBrowser2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/08c73959-d884-4870-9e6f-f1040184556f">GetDefaultMenuText</a>
</td>
<td align="left" width="63%">
Called by the Shell view to get the default shortcut menu text.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cb22504c-9f76-44c4-b81d-fc15d1b95143">GetViewFlags</a>
</td>
<td align="left" width="63%">
Called when the view must determine if special customization needs to be made for the common dialog browser.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/486c306d-90ea-4ea4-afe1-2c3f5015ccf7">Notify</a>
</td>
<td align="left" width="63%">
Called by a Shell view to notify the common dialog box hosting it that an event has occurred.

</td>
</tr>
</table> 


## -remarks



This interface also provides the methods of the <a href="https://msdn.microsoft.com/bf89ac6e-6c2e-4944-885c-9ab62f58fe71">ICommDlgBrowser</a> interface, from which it inherits.

<div class="alert"><b>Note</b>  In Windows XP and earlier, this interface was defined in Shlobj.h.</div>
<div> </div>
This interface is implemented only by common file dialog boxes.

Use <b>ICommDlgBrowser2</b> when your Shell view is hosted inside a common dialog box.

<b>ICommDlgBrowser2</b> implements all the <a href="https://msdn.microsoft.com/bf89ac6e-6c2e-4944-885c-9ab62f58fe71">ICommDlgBrowser</a> methods, as well as <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>. The listed methods are specific to <b>ICommDlgBrowser2</b>.

<div class="alert"><b>Note</b>  <b>Windows Vista and later.</b> Prior to Windows Vista this interface was declared in Shlobj.h.</div>
<div> </div>


