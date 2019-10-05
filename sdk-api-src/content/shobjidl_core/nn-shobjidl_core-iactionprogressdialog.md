---
UID: NN:shobjidl_core.IActionProgressDialog
title: IActionProgressDialog (shobjidl_core.h)
author: windows-sdk-content
description: Exposes methods that initialize and stop a progress dialog.
old-location: shell\IActionProgressDialog.htm
tech.root: shell
ms.assetid: f3c0e4ae-f93f-4ee2-873a-d9370044e922
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IActionProgressDialog, IActionProgressDialog interface [Windows Shell], IActionProgressDialog interface [Windows Shell],described, _shell_IActionProgressDialog, shell.IActionProgressDialog, shobjidl_core/IActionProgressDialog
ms.topic: interface
f1_keywords: 
 - "shobjidl_core/IActionProgressDialog"
dev_langs:
 - c++
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
req.lib: 
req.dll: Browseui.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Browseui.dll
api_name:
 - IActionProgressDialog
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IActionProgressDialog interface


## -description


Exposes methods that initialize and stop a progress dialog.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IActionProgressDialog</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IActionProgressDialog</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iactionprogressdialog-initialize">Initialize</a>
</td>
<td align="left" width="63%">
Provides details about the action progress dialog.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iactionprogressdialog-stop">Stop</a>
</td>
<td align="left" width="63%">
Stops a progress dialog.

</td>
</tr>
</table> 


## -remarks



To instantiate an object that implements this interface, call <a href="https://docs.microsoft.com/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance">CoCreateInstance</a> using the class identifier (CLSID) CLSID_ProgressDialog.



