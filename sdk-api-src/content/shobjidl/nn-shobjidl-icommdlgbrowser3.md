---
UID: NN:shobjidl.ICommDlgBrowser3
title: ICommDlgBrowser3
author: windows-sdk-content
description: Extends the capabilities of ICommDlgBrowser2, and used by the common file dialog boxes when they host a Shell browser.
old-location: shell\ICommDlgBrowser3.htm
old-project: shell
ms.assetid: c9286061-8ac8-452b-9204-193bc6b571cb
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: ICommDlgBrowser3, ICommDlgBrowser3 interface [Windows Shell], ICommDlgBrowser3 interface [Windows Shell],described, _shell_ICommDlgBrowser3, shell.ICommDlgBrowser3, shobjidl/ICommDlgBrowser3
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
 - Shobjidl.h
api_name:
 - ICommDlgBrowser3
product: Windows
targetos: Windows
req.lib: Shell32.lib
req.dll: Shell32.dll
req.irql: 
req.product: Internet Explorer 6.01
---

# ICommDlgBrowser3 interface


## -description


Extends the capabilities of <a href="https://msdn.microsoft.com/07a416a2-340d-4308-a6f3-cf6f19f3c906">ICommDlgBrowser2</a>, and used by the common file dialog boxes when they host a Shell browser.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICommDlgBrowser3</b> interface inherits from <a href="https://msdn.microsoft.com/07a416a2-340d-4308-a6f3-cf6f19f3c906">ICommDlgBrowser2</a>. <b>ICommDlgBrowser3</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ICommDlgBrowser3</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/038f3478-82d0-4023-a787-b7a2c66ceb27">GetCurrentFilter</a>
</td>
<td align="left" width="63%">
Gets the current filter as a Unicode string.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/19cd3dc6-14e4-494d-b4d7-2c9d4fd0fe55">OnColumnClicked</a>
</td>
<td align="left" width="63%">
Called after a specified column is clicked in the <a href="https://msdn.microsoft.com/91438583-e4f1-456f-a130-2a45846fd725">IShellView</a> interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1506f553-e0b0-4d6b-9d63-15f3a2d38112">OnPreViewCreated</a>
</td>
<td align="left" width="63%">
Called after a specified preview is created in the <a href="https://msdn.microsoft.com/91438583-e4f1-456f-a130-2a45846fd725">IShellView</a> interface.

</td>
</tr>
</table> 


## -remarks



This interface also provides the methods of the <a href="https://msdn.microsoft.com/bf89ac6e-6c2e-4944-885c-9ab62f58fe71">ICommDlgBrowser</a> and <a href="https://msdn.microsoft.com/07a416a2-340d-4308-a6f3-cf6f19f3c906">ICommDlgBrowser2</a> interfaces, from which it inherits.

A pointer to <b>ICommDlgBrowser3</b> can be obtained by calling <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">QueryInterface</a> on the <a href="https://msdn.microsoft.com/07a416a2-340d-4308-a6f3-cf6f19f3c906">ICommDlgBrowser2</a> object.



