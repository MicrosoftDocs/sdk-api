---
UID: NF:shobjidl_core.IIOCancelInformation.SetCancelInformation
title: IIOCancelInformation::SetCancelInformation (shobjidl_core.h)
description: Sets information that is posted when a user selects Cancel from the progress UI.
helpviewer_keywords: ["IIOCancelInformation interface [Windows Shell]","SetCancelInformation method","IIOCancelInformation.SetCancelInformation","IIOCancelInformation::SetCancelInformation","SetCancelInformation","SetCancelInformation method [Windows Shell]","SetCancelInformation method [Windows Shell]","IIOCancelInformation interface","_shell_IIOCancelInformation_SetCancelInformation","shell.IIOCancelInformation_SetCancelInformation","shobjidl_core/IIOCancelInformation::SetCancelInformation"]
old-location: shell\IIOCancelInformation_SetCancelInformation.htm
tech.root: shell
ms.assetid: ed7a2a43-8944-4e17-af0a-d64f0cb493e6
ms.date: 12/05/2018
ms.keywords: IIOCancelInformation interface [Windows Shell],SetCancelInformation method, IIOCancelInformation.SetCancelInformation, IIOCancelInformation::SetCancelInformation, SetCancelInformation, SetCancelInformation method [Windows Shell], SetCancelInformation method [Windows Shell],IIOCancelInformation interface, _shell_IIOCancelInformation_SetCancelInformation, shell.IIOCancelInformation_SetCancelInformation, shobjidl_core/IIOCancelInformation::SetCancelInformation
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
 - IIOCancelInformation::SetCancelInformation
 - shobjidl_core/IIOCancelInformation::SetCancelInformation
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
 - IIOCancelInformation.SetCancelInformation
---

# IIOCancelInformation::SetCancelInformation


## -description

Sets information that is posted when a user selects <b>Cancel</b> from the progress UI. Allows the main object to tell the progress dialog thread about the process thread so that the progress dialog can send the process thread the message id when the user clicks <b>Cancel</b>.

## -parameters

### -param dwThreadID [in]

Type: <b>DWORD</b>

The ID of the process thread to be canceled.

### -param uMsgCancel [in]

Type: <b>UINT</b>

The cancel message to be posted to the thread.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

 When the user selects <b>Cancel</b> from the progress UI, the <i>dwThreadID</i> will cancel any pending or future input/output (I/O) requests.  Also the <i>uMsgCancel</i> message, received from the progress dialog, will be posted to the thread to tell it to exit a wait state, if asynchronous I/O is pending.

