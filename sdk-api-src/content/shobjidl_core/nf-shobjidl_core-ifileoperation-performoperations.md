---
UID: NF:shobjidl_core.IFileOperation.PerformOperations
title: IFileOperation::PerformOperations (shobjidl_core.h)
description: Executes all selected operations.
helpviewer_keywords: ["IFileOperation interface [Windows Shell]","PerformOperations method","IFileOperation.PerformOperations","IFileOperation::PerformOperations","PerformOperations","PerformOperations method [Windows Shell]","PerformOperations method [Windows Shell]","IFileOperation interface","_shell_IFileOperation_PerformOperations","shell.IFileOperation_PerformOperations","shobjidl_core/IFileOperation::PerformOperations"]
old-location: shell\IFileOperation_PerformOperations.htm
tech.root: shell
ms.assetid: eceb5f0a-ad9a-4b7a-9656-c10e0420a96a
ms.date: 12/05/2018
ms.keywords: IFileOperation interface [Windows Shell],PerformOperations method, IFileOperation.PerformOperations, IFileOperation::PerformOperations, PerformOperations, PerformOperations method [Windows Shell], PerformOperations method [Windows Shell],IFileOperation interface, _shell_IFileOperation_PerformOperations, shell.IFileOperation_PerformOperations, shobjidl_core/IFileOperation::PerformOperations
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
 - IFileOperation::PerformOperations
 - shobjidl_core/IFileOperation::PerformOperations
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
 - IFileOperation.PerformOperations
---

# IFileOperation::PerformOperations


## -description

Executes all selected operations.



## -returns

Type: <b>HRESULT</b>

Returns S_OK if successful, or an error value otherwise. Note that if the operation was canceled by the user, this method can still return a success code. Use the <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifileoperation-getanyoperationsaborted">GetAnyOperationsAborted</a> method to determine if this was the case.

## -remarks

This method is called last to execute those actions that have been specified earlier by calling their individual methods. For instance, <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifileoperation-renameitem">RenameItem</a> does not rename the item, it simply sets the parameters. The actual renaming is done when you call <b>PerformOperations</b>.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifileoperationprogresssink-finishoperations">FinishOperations</a>



<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileoperation">IFileOperation</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifileoperationprogresssink-startoperations">StartOperations</a>
