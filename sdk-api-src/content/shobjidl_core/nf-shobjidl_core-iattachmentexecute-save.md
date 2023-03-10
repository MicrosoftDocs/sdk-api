---
UID: NF:shobjidl_core.IAttachmentExecute.Save
title: IAttachmentExecute::Save (shobjidl_core.h)
description: Saves the attachment.
helpviewer_keywords: ["IAttachmentExecute interface [Windows Shell]","Save method","IAttachmentExecute.Save","IAttachmentExecute::Save","Save","Save method [Windows Shell]","Save method [Windows Shell]","IAttachmentExecute interface","_win32_IAttachmentExecute_Save","shell.IAttachmentExecute_Save","shobjidl_core/IAttachmentExecute::Save"]
old-location: shell\IAttachmentExecute_Save.htm
tech.root: shell
ms.assetid: 25661942-f38b-42d6-981b-4a3f4d083f6c
ms.date: 12/05/2018
ms.keywords: IAttachmentExecute interface [Windows Shell],Save method, IAttachmentExecute.Save, IAttachmentExecute::Save, Save, Save method [Windows Shell], Save method [Windows Shell],IAttachmentExecute interface, _win32_IAttachmentExecute_Save, shell.IAttachmentExecute_Save, shobjidl_core/IAttachmentExecute::Save
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
 - IAttachmentExecute::Save
 - shobjidl_core/IAttachmentExecute::Save
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
 - IAttachmentExecute.Save
---

# IAttachmentExecute::Save


## -description

Saves the attachment.



## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Before calling <b>IAttachmentExecute::Save</b>, you must call <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iattachmentexecute-setlocalpath">IAttachmentExecute::SetLocalPath</a> with a valid path. The file should be copied to that local path before <b>IAttachmentExecute::Save</b> is called.

<b>IAttachmentExecute::Save</b> should always be called if the local path declared in <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iattachmentexecute-setlocalpath">IAttachmentExecute::SetLocalPath</a> is not the path of a temporary directory.

<b>IAttachmentExecute::Save</b> may run virus scanners or other trust services to validate the file before saving it. Note that these services can delete or alter the file.

<b>IAttachmentExecute::Save</b> may attach <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iattachmentexecute-checkpolicy">evidence</a> to the local path in its NTFS alternate data stream (ADS).

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iattachmentexecute">IAttachmentExecute</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iattachmentexecute-savewithui">IAttachmentExecute::SaveWithUI</a>
