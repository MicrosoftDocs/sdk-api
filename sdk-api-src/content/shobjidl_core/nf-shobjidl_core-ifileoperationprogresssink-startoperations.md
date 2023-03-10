---
UID: NF:shobjidl_core.IFileOperationProgressSink.StartOperations
title: IFileOperationProgressSink::StartOperations (shobjidl_core.h)
description: Performs caller-implemented actions before any specific file operations are performed.
helpviewer_keywords: ["IFileOperationProgressSink interface [Windows Shell]","StartOperations method","IFileOperationProgressSink.StartOperations","IFileOperationProgressSink::StartOperations","StartOperations","StartOperations method [Windows Shell]","StartOperations method [Windows Shell]","IFileOperationProgressSink interface","_shell_IFileOperationProgressSink_StartOperations","shell.IFileOperationProgressSink_StartOperations","shobjidl_core/IFileOperationProgressSink::StartOperations"]
old-location: shell\IFileOperationProgressSink_StartOperations.htm
tech.root: shell
ms.assetid: 8b9e4423-ead7-44be-b960-5ee83025f42a
ms.date: 12/05/2018
ms.keywords: IFileOperationProgressSink interface [Windows Shell],StartOperations method, IFileOperationProgressSink.StartOperations, IFileOperationProgressSink::StartOperations, StartOperations, StartOperations method [Windows Shell], StartOperations method [Windows Shell],IFileOperationProgressSink interface, _shell_IFileOperationProgressSink_StartOperations, shell.IFileOperationProgressSink_StartOperations, shobjidl_core/IFileOperationProgressSink::StartOperations
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
 - IFileOperationProgressSink::StartOperations
 - shobjidl_core/IFileOperationProgressSink::StartOperations
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
 - IFileOperationProgressSink.StartOperations
---

# IFileOperationProgressSink::StartOperations


## -description

Performs caller-implemented actions before any specific file operations are performed.



## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

<b>StartOperations</b> is the first of the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileoperationprogresssink">IFileOperationProgressSink</a> methods to be called after <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifileoperation-performoperations">PerformOperations</a>. It can be used to perform any setup or initialization that you require before the file operations begin.
