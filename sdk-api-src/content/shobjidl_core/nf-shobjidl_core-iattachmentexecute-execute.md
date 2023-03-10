---
UID: NF:shobjidl_core.IAttachmentExecute.Execute
title: IAttachmentExecute::Execute (shobjidl_core.h)
description: Executes an action on an attachment.
helpviewer_keywords: ["Execute","Execute method [Windows Shell]","Execute method [Windows Shell]","IAttachmentExecute interface","IAttachmentExecute interface [Windows Shell]","Execute method","IAttachmentExecute.Execute","IAttachmentExecute::Execute","_win32_IAttachmentExecute_Execute","shell.IAttachmentExecute_Execute","shobjidl_core/IAttachmentExecute::Execute"]
old-location: shell\IAttachmentExecute_Execute.htm
tech.root: shell
ms.assetid: 80cbbb6c-c6f1-4937-9c1e-4de57aee748c
ms.date: 12/05/2018
ms.keywords: Execute, Execute method [Windows Shell], Execute method [Windows Shell],IAttachmentExecute interface, IAttachmentExecute interface [Windows Shell],Execute method, IAttachmentExecute.Execute, IAttachmentExecute::Execute, _win32_IAttachmentExecute_Execute, shell.IAttachmentExecute_Execute, shobjidl_core/IAttachmentExecute::Execute
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2 [desktop apps only]
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
req.dll: Shdocvw.dll (version 6.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IAttachmentExecute::Execute
 - shobjidl_core/IAttachmentExecute::Execute
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shdocvw.dll
api_name:
 - IAttachmentExecute.Execute
---

# IAttachmentExecute::Execute


## -description

Executes an action on an attachment.

## -parameters

### -param hwnd [in]

Type: <b>HWND</b>

The handle of the parent window.

### -param pszVerb [in, optional]

Type: <b>LPCWSTR</b>

A pointer to a null-terminated string that contains a verb specifying the action to be performed on the file. See the <i>lpOperation</i> parameter in <a href="/windows/desktop/api/shellapi/nf-shellapi-shellexecutea">ShellExecute</a> for valid strings. This value can be <b>NULL</b>.

### -param phProcess [out, optional]

Type: <b>HANDLE*</b>

A pointer to a handle to the source process, used for synchronous operation. This value can be <b>NULL</b>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Before calling <b>IAttachmentExecute::Execute</b>, <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iattachmentexecute-setlocalpath">IAttachmentExecute::SetLocalPath</a> must be called with a valid local path and the file must be copied to that location.

If a prompt is indicated, <b>IAttachmentExecute::Execute</b> calls <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iattachmentexecute-prompt">IAttachmentExecute::Prompt</a> using the <a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-attachment_action">ATTACHMENT_ACTION_EXEC</a> value.

<b>IAttachmentExecute::Execute</b> may run virus scanners or other trust services to validate the file before executing it. Note that these services can delete or alter the file.

<b>IAttachmentExecute::Execute</b> may attach <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iattachmentexecute-checkpolicy">evidence</a> to the local path in its NTFS alternate data stream (ADS).

If <i>phProcess</i> is not <b>NULL</b>, <b>IAttachmentExecute::Execute</b> operates as a synchronous process and returns an <b>HPROCESS</b>, if available. If <i>phProcess</i> is <b>NULL</b>, <b>IAttachmentExecute::Execute</b> operates as an asynchronous process. This implies that the calling application has a message pump and a long-lived window.

If the handle pointed to by <i>phProcess</i> is non-<b>NULL</b> when the method returns, the calling application is responsible for calling <a href="/windows/desktop/api/handleapi/nf-handleapi-closehandle">CloseHandle</a> to free the handle when it is no longer needed.