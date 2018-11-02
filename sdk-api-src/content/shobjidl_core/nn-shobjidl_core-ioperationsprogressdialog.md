---
UID: NN:shobjidl_core.IOperationsProgressDialog
title: IOperationsProgressDialog
author: windows-sdk-content
description: Exposes methods to get, set, and query a progress dialog.
old-location: shell\IOperationsProgressDialog.htm
tech.root: shell
ms.assetid: 0d95f407-0e09-441d-b9e2-665995ea1362
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: IOperationsProgressDialog, IOperationsProgressDialog interface [Windows Shell], IOperationsProgressDialog interface [Windows Shell],described, _shell_IOperationsProgressDialog, shell.IOperationsProgressDialog, shobjidl_core/IOperationsProgressDialog
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - IOperationsProgressDialog
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IOperationsProgressDialog interface


## -description


Exposes methods to get, set, and query a progress dialog.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IOperationsProgressDialog</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IOperationsProgressDialog</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/0e1c34cf-1fa2-43b7-91c9-2ec9224b5b39">GetMilliseconds</a>
</td>
<td align="left" width="63%">
Gets elapsed and remaining time for progress dialog.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bd796369-9789-4c69-b699-eb0ec0e571b2">GetOperationStatus</a>
</td>
<td align="left" width="63%">
Gets operation status for progress dialog.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9fdfd3b1-23fb-4172-a3e4-2142a29c21e3">PauseTimer</a>
</td>
<td align="left" width="63%">
Pauses progress dialog timer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a16d1595-c601-45a0-b3f5-35fe31cd0f22">ResetTimer</a>
</td>
<td align="left" width="63%">
Resets progress dialog timer to 0.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c2f219f8-75c0-4101-a499-2770bb01ab7b">ResumeTimer</a>
</td>
<td align="left" width="63%">
Resumes progress dialog timer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ec731281-c0af-4cf6-aa63-d80a80a18c15">SetMode</a>
</td>
<td align="left" width="63%">
Sets progress dialog operations mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b6fae1df-1c27-4ce9-a7f6-c5488f080ef3">SetOperation</a>
</td>
<td align="left" width="63%">
Sets which progress dialog operation is occurring, and whether we are in pre-flight or undo mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5d6f44e0-259f-42d3-9912-877d90f0e7fc">StartProgressDialog</a>
</td>
<td align="left" width="63%">
Starts the specified progress dialog.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1033b197-f11c-49ed-8186-914c1cb04250">StopProgressDialog</a>
</td>
<td align="left" width="63%">
Stops current progress dialog.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/df07833a-691c-4d93-a85e-8d21dd04ee64">UpdateLocations</a>
</td>
<td align="left" width="63%">
Called to specify the text elements stating the source and target in the current progress dialog.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5ff2def3-f320-412c-8f98-bd1a58866d03">UpdateProgress</a>
</td>
<td align="left" width="63%">
Updates the current progress dialog, as specified.

</td>
</tr>
</table> 

