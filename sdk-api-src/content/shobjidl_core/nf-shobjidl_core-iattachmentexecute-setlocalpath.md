---
UID: NF:shobjidl_core.IAttachmentExecute.SetLocalPath
title: IAttachmentExecute::SetLocalPath (shobjidl_core.h)
description: Sets and stores the path to the file.
helpviewer_keywords: ["IAttachmentExecute interface [Windows Shell]","SetLocalPath method","IAttachmentExecute.SetLocalPath","IAttachmentExecute::SetLocalPath","SetLocalPath","SetLocalPath method [Windows Shell]","SetLocalPath method [Windows Shell]","IAttachmentExecute interface","_win32_IAttachmentExecute_SetLocalPath","shell.IAttachmentExecute_SetLocalPath","shobjidl_core/IAttachmentExecute::SetLocalPath"]
old-location: shell\IAttachmentExecute_SetLocalPath.htm
tech.root: shell
ms.assetid: 763ce5a7-bbad-4dd8-a416-86a96f466510
ms.date: 12/05/2018
ms.keywords: IAttachmentExecute interface [Windows Shell],SetLocalPath method, IAttachmentExecute.SetLocalPath, IAttachmentExecute::SetLocalPath, SetLocalPath, SetLocalPath method [Windows Shell], SetLocalPath method [Windows Shell],IAttachmentExecute interface, _win32_IAttachmentExecute_SetLocalPath, shell.IAttachmentExecute_SetLocalPath, shobjidl_core/IAttachmentExecute::SetLocalPath
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
 - IAttachmentExecute::SetLocalPath
 - shobjidl_core/IAttachmentExecute::SetLocalPath
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
 - IAttachmentExecute.SetLocalPath
---

# IAttachmentExecute::SetLocalPath


## -description

Sets and stores the path to the file.

## -parameters

### -param pszLocalPath [in]

Type: <b>LPCWSTR</b>

A pointer to a string that contains the local path where the attachment file is to be stored.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Calling <b>IAttachmentExecute::SetLocalPath</b> is required.

When the attachment is approved for execution by the user (either through policy or prompt), the path specified by this method is used. If only <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iattachmentexecute-setfilename">IAttachmentExecute::SetFileName</a> was called before calling <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iattachmentexecute-checkpolicy">IAttachmentExecute::CheckPolicy</a> and <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iattachmentexecute-prompt">IAttachmentExecute::Prompt</a>, that trust could be revoked if the assumed local path was different from that set by <b>IAttachmentExecute::SetLocalPath</b>. Trust can be granted by various Zone APIs, antivirus services, file type information, policies as well as other system trust providers.

<b>IAttachmentExecute::SetLocalPath</b> must be called before calling <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iattachmentexecute-execute">IAttachmentExecute::Execute</a>.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iattachmentexecute">IAttachmentExecute</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iattachmentexecute-setfilename">IAttachmentExecute::SetFileName</a>