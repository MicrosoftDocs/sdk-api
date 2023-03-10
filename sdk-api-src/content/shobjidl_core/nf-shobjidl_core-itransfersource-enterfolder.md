---
UID: NF:shobjidl_core.ITransferSource.EnterFolder
title: ITransferSource::EnterFolder (shobjidl_core.h)
description: Notifies that a folder is the destination of a file operation.
helpviewer_keywords: ["EnterFolder","EnterFolder method [Windows Shell]","EnterFolder method [Windows Shell]","ITransferSource interface","ITransferSource interface [Windows Shell]","EnterFolder method","ITransferSource.EnterFolder","ITransferSource::EnterFolder","_shell_ITransferSource_EnterFolder","shell.ITransferSource_EnterFolder","shobjidl_core/ITransferSource::EnterFolder"]
old-location: shell\ITransferSource_EnterFolder.htm
tech.root: shell
ms.assetid: de6b1b03-450f-4d48-b0f4-67e268feb36a
ms.date: 12/05/2018
ms.keywords: EnterFolder, EnterFolder method [Windows Shell], EnterFolder method [Windows Shell],ITransferSource interface, ITransferSource interface [Windows Shell],EnterFolder method, ITransferSource.EnterFolder, ITransferSource::EnterFolder, _shell_ITransferSource_EnterFolder, shell.ITransferSource_EnterFolder, shobjidl_core/ITransferSource::EnterFolder
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITransferSource::EnterFolder
 - shobjidl_core/ITransferSource::EnterFolder
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - ITransferSource.EnterFolder
---

# ITransferSource::EnterFolder


## -description

Notifies that a folder is the destination of a file operation.

## -parameters

### -param psiChildFolderDest [in]

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a>*</b>

A pointer to the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a> destination folder.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

 This method is called when beginning to process a folder or subfolder in a recursive operation. For instance, when a source folder is copied to a destination folder, method <b>ITransferSource::EnterFolder</b> should be called with <i>psiChildFolderDest</i> set to the destination folder.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-itransfersource">ITransferSource</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itransfersource-advise">ITransferSource::Advise</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itransfersource-leavefolder">ITransferSource::LeaveFolder</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itransfersource-unadvise">ITransferSource::Unadvise</a>