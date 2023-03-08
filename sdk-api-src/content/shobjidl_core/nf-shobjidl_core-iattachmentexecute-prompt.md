---
UID: NF:shobjidl_core.IAttachmentExecute.Prompt
title: IAttachmentExecute::Prompt (shobjidl_core.h)
description: Presents a prompt UI to the user.
helpviewer_keywords: ["IAttachmentExecute interface [Windows Shell]","Prompt method","IAttachmentExecute.Prompt","IAttachmentExecute::Prompt","Prompt","Prompt method [Windows Shell]","Prompt method [Windows Shell]","IAttachmentExecute interface","_win32_IAttachmentExecute_Prompt","shell.IAttachmentExecute_Prompt","shobjidl_core/IAttachmentExecute::Prompt"]
old-location: shell\IAttachmentExecute_Prompt.htm
tech.root: shell
ms.assetid: 01c01abf-df7a-411b-979b-ddd8da569f91
ms.date: 12/05/2018
ms.keywords: IAttachmentExecute interface [Windows Shell],Prompt method, IAttachmentExecute.Prompt, IAttachmentExecute::Prompt, Prompt, Prompt method [Windows Shell], Prompt method [Windows Shell],IAttachmentExecute interface, _win32_IAttachmentExecute_Prompt, shell.IAttachmentExecute_Prompt, shobjidl_core/IAttachmentExecute::Prompt
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
 - IAttachmentExecute::Prompt
 - shobjidl_core/IAttachmentExecute::Prompt
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
 - IAttachmentExecute.Prompt
---

# IAttachmentExecute::Prompt


## -description

Presents a prompt UI to the user.

## -parameters

### -param hwnd [in]

Type: <b>HWND</b>

A handle to the parent window.

### -param prompt [in]

Type: <b><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-attachment_prompt">ATTACHMENT_PROMPT</a></b>

A member of the <a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-attachment_prompt">ATTACHMENT_PROMPT</a> enumeration that indicates what type of prompt UI to display to the user.

### -param paction [out]

Type: <b><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-attachment_action">ATTACHMENT_ACTION</a>*</b>

A member of the <a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-attachment_action">ATTACHMENT_ACTION</a> enumeration that indicates the action to be performed upon user confirmation.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

You must call <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iattachmentexecute-setfilename">IAttachmentExecute::SetFileName</a> or <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iattachmentexecute-setlocalpath">IAttachmentExecute::SetLocalPath</a> before calling <b>IAttachmentExecute::Prompt</b>.

<b>IAttachmentExecute::Prompt</b> can be called by the application to force UI presentation before the file has been copied to disk.