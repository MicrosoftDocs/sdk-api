---
UID: NF:shobjidl_core.IAttachmentExecute.SaveWithUI
title: IAttachmentExecute::SaveWithUI (shobjidl_core.h)
description: Presents the user with explanatory error UI if the save action fails.
helpviewer_keywords: ["IAttachmentExecute interface [Windows Shell]","SaveWithUI method","IAttachmentExecute.SaveWithUI","IAttachmentExecute::SaveWithUI","SaveWithUI","SaveWithUI method [Windows Shell]","SaveWithUI method [Windows Shell]","IAttachmentExecute interface","shell.IAttachmentExecute_SaveWithUI","shell_IAttachmentExecute_savewithui","shobjidl_core/IAttachmentExecute::SaveWithUI"]
old-location: shell\IAttachmentExecute_SaveWithUI.htm
tech.root: shell
ms.assetid: 6d5b2d02-98ee-4e46-826f-fa073ecff5c4
ms.date: 12/05/2018
ms.keywords: IAttachmentExecute interface [Windows Shell],SaveWithUI method, IAttachmentExecute.SaveWithUI, IAttachmentExecute::SaveWithUI, SaveWithUI, SaveWithUI method [Windows Shell], SaveWithUI method [Windows Shell],IAttachmentExecute interface, shell.IAttachmentExecute_SaveWithUI, shell_IAttachmentExecute_savewithui, shobjidl_core/IAttachmentExecute::SaveWithUI
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
 - IAttachmentExecute::SaveWithUI
 - shobjidl_core/IAttachmentExecute::SaveWithUI
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
 - IAttachmentExecute.SaveWithUI
---

# IAttachmentExecute::SaveWithUI


## -description

Presents the user with explanatory error UI if the save action fails.

## -parameters

### -param hwnd [in]

Type: <b>HWND</b>

The handle of the parent window.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

<b>IAttachmentExecute::SaveWithUI</b> does not call <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iattachmentexecute-prompt">IAttachmentExecute::Prompt</a>.

Before calling <b>IAttachmentExecute::SaveWithUI</b>, you must call <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iattachmentexecute-setlocalpath">IAttachmentExecute::SetLocalPath</a> with a valid path. The file is copied to that local path before <b>IAttachmentExecute::SaveWithUI</b> is called.

<b>IAttachmentExecute::SaveWithUI</b> may run virus scanners or other trust services to validate the file before saving it. Note that these services can delete or alter the file.

<b>IAttachmentExecute::SaveWithUI</b> may attach <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iattachmentexecute-checkpolicy">evidence</a> to the local path in its NTFS alternate data stream (ADS).

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iattachmentexecute">IAttachmentExecute</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iattachmentexecute-save">IAttachmentExecute::Save</a>