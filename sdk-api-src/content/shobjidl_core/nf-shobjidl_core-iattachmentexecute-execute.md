---
UID: NF:shobjidl_core.IAttachmentExecute.Execute
title: IAttachmentExecute::Execute
author: windows-sdk-content
description: Executes an action on an attachment.
old-location: shell\IAttachmentExecute_Execute.htm
old-project: shell
ms.assetid: 80cbbb6c-c6f1-4937-9c1e-4de57aee748c
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: Execute, Execute method [Windows Shell], Execute method [Windows Shell],IAttachmentExecute interface, IAttachmentExecute interface [Windows Shell],Execute method, IAttachmentExecute.Execute, IAttachmentExecute::Execute, _win32_IAttachmentExecute_Execute, shell.IAttachmentExecute_Execute, shobjidl_core/IAttachmentExecute::Execute
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shdocvw.dll
api_name:
 - IAttachmentExecute.Execute
product: Windows
targetos: Windows
req.lib: 
req.dll: Shdocvw.dll (version 6.0 or later)
req.irql: 
req.product: Outlook Express 6.0
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

A pointer to a null-terminated string that contains a verb specifying the action to be performed on the file. See the <i>lpOperation</i> parameter in <a href="https://msdn.microsoft.com/8b1f3978-a0ee-4684-8a37-98e270b63897">ShellExecute</a> for valid strings. This value can be <b>NULL</b>.


### -param phProcess [out, optional]

Type: <b>HANDLE*</b>

A pointer to a handle to the source process, used for synchronous operation. This value can be <b>NULL</b>.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Before calling <b>IAttachmentExecute::Execute</b>, <a href="https://msdn.microsoft.com/763ce5a7-bbad-4dd8-a416-86a96f466510">IAttachmentExecute::SetLocalPath</a> must be called with a valid local path and the file must be copied to that location.

If a prompt is indicated, <b>IAttachmentExecute::Execute</b> calls <a href="https://msdn.microsoft.com/01c01abf-df7a-411b-979b-ddd8da569f91">IAttachmentExecute::Prompt</a> using the <a href="https://msdn.microsoft.com/2deeb14b-2665-4970-923c-9da1f561979f">ATTACHMENT_ACTION_EXEC</a> value.

<b>IAttachmentExecute::Execute</b> may run virus scanners or other trust services to validate the file before executing it. Note that these services can delete or alter the file.

<b>IAttachmentExecute::Execute</b> may attach <a href="https://msdn.microsoft.com/ff6a0aa8-4d14-4074-b084-be117b01c77a">evidence</a> to the local path in its NTFS alternate data stream (ADS).

If <i>phProcess</i> is not <b>NULL</b>, <b>IAttachmentExecute::Execute</b> operates as a synchronous process and returns an <b>HPROCESS</b>, if available. If <i>phProcess</i> is <b>NULL</b>, <b>IAttachmentExecute::Execute</b> operates as an asynchronous process. This implies that the calling application has a message pump and a long-lived window.

If the handle pointed to by <i>phProcess</i> is non-<b>NULL</b> when the method returns, the calling application is responsible for calling <a href="https://msdn.microsoft.com/9b84891d-62ca-4ddc-97b7-c4c79482abd9">CloseHandle</a> to free the handle when it is no longer needed.



