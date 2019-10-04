---
UID: NN:shobjidl_core.IIOCancelInformation
title: IIOCancelInformation (shobjidl_core.h)
author: windows-sdk-content
description: Exposes methods for posting a cancel window message to the process thread from the Progress Dialog.
old-location: shell\IIOCancelInformation.htm
tech.root: shell
ms.assetid: fb030100-b0e8-497c-b9e1-338599aa3b0f
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IIOCancelInformation, IIOCancelInformation interface [Windows Shell], IIOCancelInformation interface [Windows Shell],described, _shell_IIOCancelInformation, shell.IIOCancelInformation, shobjidl_core/IIOCancelInformation
ms.topic: interface
f1_keywords: 
 - "shobjidl_core/IIOCancelInformation"
dev_langs:
 - c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IIOCancelInformation interface


## -description


Exposes methods for posting a cancel window message to the process thread from the Progress Dialog. 



This interface enables the progress dialog to post a thread message through <a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-postthreadmessagea">PostThreadMessage</a> to the worker thread to cancel its operations. The worker thread must periodically check the message queue through <a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-getmessage">GetMessage</a>, <a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-peekmessagea">PeekMessage</a> or <a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-msgwaitformultipleobjectsex">MsgWaitForMultipleObjectsEx</a>.

The <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iiocancelinformation-setcancelinformation">IIOCancelInformation::SetCancelInformation</a> method tells the progress dialog which thread ID and what message to <a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-postthreadmessagea">PostThreadMessage</a> when the user clicks <b>Cancel</b>. A thread ID of "zero" disables the sending operation for the cancel message.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IIOCancelInformation</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IIOCancelInformation</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iiocancelinformation-getcancelinformation">GetCancelInformation</a>
</td>
<td align="left" width="63%">
Returns information that is posted when a user selects <b>Cancel</b> from the progress UI. The process thread uses this method to find out which message the progress dialog will send to the process thread when the user hits cancel.  The process thread then listens for this message and does its own cleanup upon receipt.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iiocancelinformation-setcancelinformation">SetCancelInformation</a>
</td>
<td align="left" width="63%">
Sets information that is posted when a user selects <b>Cancel</b> from the progress UI. Allows the main object to tell the progress dialog thread about the process thread so that the progress dialog can send the process thread the message id when the user clicks <b>Cancel</b>.


</td>
</tr>
</table> 

