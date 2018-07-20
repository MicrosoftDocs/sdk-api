---
UID: NN:shobjidl_core.IActionProgressDialog
title: IActionProgressDialog
author: windows-sdk-content
description: Exposes methods that initialize and stop a progress dialog.
old-location: shell\IActionProgressDialog.htm
old-project: shell
ms.assetid: f3c0e4ae-f93f-4ee2-873a-d9370044e922
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: IActionProgressDialog, IActionProgressDialog interface [Windows Shell], IActionProgressDialog interface [Windows Shell],described, _shell_IActionProgressDialog, shell.IActionProgressDialog, shobjidl_core/IActionProgressDialog
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
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
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Browseui.dll
api_name:
 - IActionProgressDialog
product: Windows
targetos: Windows
req.lib: Shell32.lib
req.dll: Browseui.dll
req.irql: 
req.product: Outlook Express 6.0
---

# IActionProgressDialog interface


## -description


Exposes methods that initialize and stop a progress dialog.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IActionProgressDialog</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IActionProgressDialog</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IActionProgressDialog</b> interface has these methods.
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
Provides details about the action progress dialog.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn927275">Stop</a>
</td>
<td align="left" width="63%">
Stops a progress dialog.

</td>
</tr>
</table> 


## -remarks



To instantiate an object that implements this interface, call <a href="https://msdn.microsoft.com/7295a55b-12c7-4ed0-a7a4-9ecee16afdec">CoCreateInstance</a> using the class identifier (CLSID) CLSID_ProgressDialog.



