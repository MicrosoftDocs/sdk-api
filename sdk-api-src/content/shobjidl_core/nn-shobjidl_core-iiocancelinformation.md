---
UID: NN:shobjidl_core.IIOCancelInformation
title: IIOCancelInformation (shobjidl_core.h)
description: Exposes methods for posting a cancel window message to the process thread from the Progress Dialog.
helpviewer_keywords: ["IIOCancelInformation","IIOCancelInformation interface [Windows Shell]","IIOCancelInformation interface [Windows Shell]","described","_shell_IIOCancelInformation","shell.IIOCancelInformation","shobjidl_core/IIOCancelInformation"]
old-location: shell\IIOCancelInformation.htm
tech.root: shell
ms.assetid: fb030100-b0e8-497c-b9e1-338599aa3b0f
ms.date: 12/05/2018
ms.keywords: IIOCancelInformation, IIOCancelInformation interface [Windows Shell], IIOCancelInformation interface [Windows Shell],described, _shell_IIOCancelInformation, shell.IIOCancelInformation, shobjidl_core/IIOCancelInformation
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IIOCancelInformation
 - shobjidl_core/IIOCancelInformation
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IIOCancelInformation
---

# IIOCancelInformation interface


## -description

Exposes methods for posting a cancel window message to the process thread from the Progress Dialog. 



This interface enables the progress dialog to post a thread message through <a href="/windows/desktop/api/winuser/nf-winuser-postthreadmessagea">PostThreadMessage</a> to the worker thread to cancel its operations. The worker thread must periodically check the message queue through <a href="/windows/desktop/api/winuser/nf-winuser-getmessage">GetMessage</a>, <a href="/windows/desktop/api/winuser/nf-winuser-peekmessagea">PeekMessage</a> or <a href="/windows/desktop/api/winuser/nf-winuser-msgwaitformultipleobjectsex">MsgWaitForMultipleObjectsEx</a>.

The <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iiocancelinformation-setcancelinformation">IIOCancelInformation::SetCancelInformation</a> method tells the progress dialog which thread ID and what message to <a href="/windows/desktop/api/winuser/nf-winuser-postthreadmessagea">PostThreadMessage</a> when the user clicks <b>Cancel</b>. A thread ID of "zero" disables the sending operation for the cancel message.

## -inheritance

The <b>IIOCancelInformation</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IIOCancelInformation</b> also has these types of members:

