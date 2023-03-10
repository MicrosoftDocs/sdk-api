---
UID: NF:shobjidl_core.IFileOperation.Advise
title: IFileOperation::Advise (shobjidl_core.h)
description: Enables a handler to provide status and error information for all operations.
helpviewer_keywords: ["Advise","Advise method [Windows Shell]","Advise method [Windows Shell]","IFileOperation interface","IFileOperation interface [Windows Shell]","Advise method","IFileOperation.Advise","IFileOperation::Advise","_shell_IFileOperation_Advise","shell.IFileOperation_Advise","shobjidl_core/IFileOperation::Advise"]
old-location: shell\IFileOperation_Advise.htm
tech.root: shell
ms.assetid: 458c24b0-9288-4ed7-9a4b-7534f26dd32e
ms.date: 12/05/2018
ms.keywords: Advise, Advise method [Windows Shell], Advise method [Windows Shell],IFileOperation interface, IFileOperation interface [Windows Shell],Advise method, IFileOperation.Advise, IFileOperation::Advise, _shell_IFileOperation_Advise, shell.IFileOperation_Advise, shobjidl_core/IFileOperation::Advise
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
 - IFileOperation::Advise
 - shobjidl_core/IFileOperation::Advise
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
 - IFileOperation.Advise
---

# IFileOperation::Advise


## -description

Enables a handler to provide status and error information for all operations.

## -parameters

### -param pfops [in]

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileoperationprogresssink">IFileOperationProgressSink</a>*</b>

Pointer to an <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileoperationprogresssink">IFileOperationProgressSink</a> object to be used for progress status and error notifications.

### -param pdwCookie [out]

Type: <b>DWORD*</b>

When this method returns, this parameter points to a returned token that uniquely identifies this connection. The calling application uses this token later to delete the connection by passing it to <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifileoperation-unadvise">IFileOperation::Unadvise</a>. If the call to <b>Advise</b> fails, this value is meaningless.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Several individual methods have the ability to declare their own progress sinks, which are redundant to the one set here. They are used when you only want to be given progress and error information for a specific operation.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileoperation">IFileOperation</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifileoperation-unadvise">IFileOperation::Unadvise</a>