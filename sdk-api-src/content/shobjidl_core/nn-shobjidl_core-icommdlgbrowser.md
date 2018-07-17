---
UID: NN:shobjidl_core.ICommDlgBrowser
title: ICommDlgBrowser
author: windows-sdk-content
description: Exposed by the common file dialog boxes to be used when they host a Shell browser.
old-location: shell\ICommDlgBrowser.htm
old-project: shell
ms.assetid: bf89ac6e-6c2e-4944-885c-9ab62f58fe71
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: ICommDlgBrowser, ICommDlgBrowser interface [Windows Shell], ICommDlgBrowser interface [Windows Shell],described, _win32_ICommDlgBrowser, shell.ICommDlgBrowser, shobjidl_core/ICommDlgBrowser
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - Shell32.dll
api_name:
 - ICommDlgBrowser
product: Windows
targetos: Windows
req.lib: Twinapi.lib
req.dll: Shell32.dll (version 4.0 or later)
req.irql: 
req.product: Outlook Express 6.0
---

# ICommDlgBrowser interface


## -description


Exposed by the common file dialog boxes to be used when they host a Shell browser. If supported, <b>ICommDlgBrowser</b> exposes methods that allow a Shell view to handle several cases that require different behavior in a dialog box than in a normal Shell view. You obtain an <b>ICommDlgBrowser</b> interface pointer by calling <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">QueryInterface</a> on the <a href="https://msdn.microsoft.com/138d90e3-a1f0-4faf-88ca-16c7a46df0ca">IShellBrowser</a> object.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICommDlgBrowser</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ICommDlgBrowser</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ICommDlgBrowser</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f483dda2-5384-42b5-97ca-c7c6793d19a7">IncludeObject</a>
</td>
<td align="left" width="63%">
Allows the common dialog box to filter objects that the view displays.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/827af758-63df-42bb-9ecf-087bc974710a">OnDefaultCommand</a>
</td>
<td align="left" width="63%">
Called when a user double-clicks in the view or presses the ENTER key.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ec9f0e5d-ca64-4ab4-b2cc-6d0748ede8b2">OnStateChange</a>
</td>
<td align="left" width="63%">
Called after a state, identified by the <i>uChange</i> parameter, has changed in the <a href="https://msdn.microsoft.com/91438583-e4f1-456f-a130-2a45846fd725">IShellView</a> interface.

</td>
</tr>
</table> 


## -remarks



<div class="alert"><b>Note</b>  
        In Windows XP and earlier, this interface was defined in Shlobj.h.
      </div>
<div> </div>
This interface is implemented only by the common file dialog boxes.


        Use <b>ICommDlgBrowser</b> when you need to provide special behavior while hosted inside the common dialog boxes.
      



