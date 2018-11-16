---
UID: NN:shobjidl_core.IIOCancelInformation
title: IIOCancelInformation
author: windows-sdk-content
description: Exposes methods for posting a cancel window message to the process thread from the Progress Dialog.
old-location: shell\IIOCancelInformation.htm
tech.root: shell
ms.assetid: fb030100-b0e8-497c-b9e1-338599aa3b0f
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IIOCancelInformation, IIOCancelInformation interface [Windows Shell], IIOCancelInformation interface [Windows Shell],described, _shell_IIOCancelInformation, shell.IIOCancelInformation, shobjidl_core/IIOCancelInformation
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Shell32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IIOCancelInformation
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IIOCancelInformation interface


## -description


Exposes methods for posting a cancel window message to the process thread from the Progress Dialog. 



This interface enables the progress dialog to post a thread message through <a href="https://msdn.microsoft.com/c418cb0e-1b9f-4ca8-8b02-e6901f7744a6">PostThreadMessage</a> to the worker thread to cancel its operations. The worker thread must periodically check the message queue through <a href="https://msdn.microsoft.com/e92266a7-86ac-43f4-b0eb-762e145a1017">GetMessage</a>, <a href="https://msdn.microsoft.com/b9f5baa4-8166-4d6e-b416-df023aed9bad">PeekMessage</a> or <a href="https://msdn.microsoft.com/1774b721-3ad4-492e-96af-b71de9066f0c">MsgWaitForMultipleObjectsEx</a>.

The <a href="https://msdn.microsoft.com/ed7a2a43-8944-4e17-af0a-d64f0cb493e6">IIOCancelInformation::SetCancelInformation</a> method tells the progress dialog which thread ID and what message to <a href="https://msdn.microsoft.com/c418cb0e-1b9f-4ca8-8b02-e6901f7744a6">PostThreadMessage</a> when the user clicks <b>Cancel</b>. A thread ID of "zero" disables the sending operation for the cancel message.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IIOCancelInformation</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IIOCancelInformation</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IIOCancelInformation</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/201537b5-1866-4df6-a51d-3f07c18fe0c8">GetCancelInformation</a>
</td>
<td align="left" width="63%">
Returns information that is posted when a user selects <b>Cancel</b> from the progress UI. The process thread uses this method to find out which message the progress dialog will send to the process thread when the user hits cancel.  The process thread then listens for this message and does its own cleanup upon receipt.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ed7a2a43-8944-4e17-af0a-d64f0cb493e6">SetCancelInformation</a>
</td>
<td align="left" width="63%">
Sets information that is posted when a user selects <b>Cancel</b> from the progress UI. Allows the main object to tell the progress dialog thread about the process thread so that the progress dialog can send the process thread the message id when the user clicks <b>Cancel</b>.


</td>
</tr>
</table> 

