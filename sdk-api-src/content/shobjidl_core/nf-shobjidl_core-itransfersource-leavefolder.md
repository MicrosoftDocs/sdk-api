---
UID: NF:shobjidl_core.ITransferSource.LeaveFolder
title: ITransferSource::LeaveFolder (shobjidl_core.h)
description: Sends notification that a folder is no longer the destination of a file operation.
helpviewer_keywords: ["ITransferSource interface [Windows Shell]","LeaveFolder method","ITransferSource.LeaveFolder","ITransferSource::LeaveFolder","LeaveFolder","LeaveFolder method [Windows Shell]","LeaveFolder method [Windows Shell]","ITransferSource interface","_shell_ITransferSource_LeaveFolder","shell.ITransferSource_LeaveFolder","shobjidl_core/ITransferSource::LeaveFolder"]
old-location: shell\ITransferSource_LeaveFolder.htm
tech.root: shell
ms.assetid: c8d0b757-a103-4c18-b556-8ba4ea9b3a2d
ms.date: 12/05/2018
ms.keywords: ITransferSource interface [Windows Shell],LeaveFolder method, ITransferSource.LeaveFolder, ITransferSource::LeaveFolder, LeaveFolder, LeaveFolder method [Windows Shell], LeaveFolder method [Windows Shell],ITransferSource interface, _shell_ITransferSource_LeaveFolder, shell.ITransferSource_LeaveFolder, shobjidl_core/ITransferSource::LeaveFolder
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
 - ITransferSource::LeaveFolder
 - shobjidl_core/ITransferSource::LeaveFolder
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
 - ITransferSource.LeaveFolder
---

# ITransferSource::LeaveFolder


## -description

Sends notification that a folder is no longer the destination of a file operation.

## -parameters

### -param psiChildFolderDest [in]

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a>*</b>

A pointer to the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a> destination folder.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This method is called at the end of recursive file operations on a destination folder.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-itransfersource">ITransferSource</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itransfersource-advise">ITransferSource::Advise</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itransfersource-enterfolder">ITransferSource::EnterFolder</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itransfersource-unadvise">ITransferSource::Unadvise</a>