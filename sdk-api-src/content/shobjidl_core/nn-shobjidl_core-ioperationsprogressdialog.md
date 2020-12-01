---
UID: NN:shobjidl_core.IOperationsProgressDialog
title: IOperationsProgressDialog (shobjidl_core.h)
description: Exposes methods to get, set, and query a progress dialog.
helpviewer_keywords: ["IOperationsProgressDialog","IOperationsProgressDialog interface [Windows Shell]","IOperationsProgressDialog interface [Windows Shell]","described","_shell_IOperationsProgressDialog","shell.IOperationsProgressDialog","shobjidl_core/IOperationsProgressDialog"]
old-location: shell\IOperationsProgressDialog.htm
tech.root: shell
ms.assetid: 0d95f407-0e09-441d-b9e2-665995ea1362
ms.date: 12/05/2018
ms.keywords: IOperationsProgressDialog, IOperationsProgressDialog interface [Windows Shell], IOperationsProgressDialog interface [Windows Shell],described, _shell_IOperationsProgressDialog, shell.IOperationsProgressDialog, shobjidl_core/IOperationsProgressDialog
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IOperationsProgressDialog
 - shobjidl_core/IOperationsProgressDialog
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
 - IOperationsProgressDialog
---

# IOperationsProgressDialog interface


## -description

Exposes methods to get, set, and query a progress dialog.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IOperationsProgressDialog</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IOperationsProgressDialog</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IOperationsProgressDialog</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ioperationsprogressdialog-getmilliseconds">GetMilliseconds</a>
</td>
<td align="left" width="63%">
Gets elapsed and remaining time for progress dialog.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ioperationsprogressdialog-getoperationstatus">GetOperationStatus</a>
</td>
<td align="left" width="63%">
Gets operation status for progress dialog.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ioperationsprogressdialog-pausetimer">PauseTimer</a>
</td>
<td align="left" width="63%">
Pauses progress dialog timer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ioperationsprogressdialog-resettimer">ResetTimer</a>
</td>
<td align="left" width="63%">
Resets progress dialog timer to 0.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ioperationsprogressdialog-resumetimer">ResumeTimer</a>
</td>
<td align="left" width="63%">
Resumes progress dialog timer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ioperationsprogressdialog-setmode">SetMode</a>
</td>
<td align="left" width="63%">
Sets progress dialog operations mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ioperationsprogressdialog-setoperation">SetOperation</a>
</td>
<td align="left" width="63%">
Sets which progress dialog operation is occurring, and whether we are in pre-flight or undo mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ioperationsprogressdialog-startprogressdialog">StartProgressDialog</a>
</td>
<td align="left" width="63%">
Starts the specified progress dialog.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ioperationsprogressdialog-stopprogressdialog">StopProgressDialog</a>
</td>
<td align="left" width="63%">
Stops current progress dialog.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ioperationsprogressdialog-updatelocations">UpdateLocations</a>
</td>
<td align="left" width="63%">
Called to specify the text elements stating the source and target in the current progress dialog.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ioperationsprogressdialog-updateprogress">UpdateProgress</a>
</td>
<td align="left" width="63%">
Updates the current progress dialog, as specified.

</td>
</tr>
</table>