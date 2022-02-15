---
UID: NF:shobjidl_core.IFileOperationProgressSink.UpdateProgress
title: IFileOperationProgressSink::UpdateProgress (shobjidl_core.h)
description: Provides an estimate of the total amount of work currently done in relation to the total amount of work.
helpviewer_keywords: ["IFileOperationProgressSink interface [Windows Shell]","UpdateProgress method","IFileOperationProgressSink.UpdateProgress","IFileOperationProgressSink::UpdateProgress","UpdateProgress","UpdateProgress method [Windows Shell]","UpdateProgress method [Windows Shell]","IFileOperationProgressSink interface","_shell_IFileOperationProgressSink_UpdateProgress","shell.IFileOperationProgressSink_UpdateProgress","shobjidl_core/IFileOperationProgressSink::UpdateProgress"]
old-location: shell\IFileOperationProgressSink_UpdateProgress.htm
tech.root: shell
ms.assetid: c61d4440-bcd3-46a7-8aeb-e5d80d0d53eb
ms.date: 12/05/2018
ms.keywords: IFileOperationProgressSink interface [Windows Shell],UpdateProgress method, IFileOperationProgressSink.UpdateProgress, IFileOperationProgressSink::UpdateProgress, UpdateProgress, UpdateProgress method [Windows Shell], UpdateProgress method [Windows Shell],IFileOperationProgressSink interface, _shell_IFileOperationProgressSink_UpdateProgress, shell.IFileOperationProgressSink_UpdateProgress, shobjidl_core/IFileOperationProgressSink::UpdateProgress
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
 - IFileOperationProgressSink::UpdateProgress
 - shobjidl_core/IFileOperationProgressSink::UpdateProgress
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
 - IFileOperationProgressSink.UpdateProgress
---

# IFileOperationProgressSink::UpdateProgress


## -description

Provides an estimate of the total amount of work currently done in relation to the total amount of work.

## -parameters

### -param iWorkTotal [in]

Type: <b>UINT</b>

An estimate of the amount of work to be completed.

### -param iWorkSoFar [in]

Type: <b>UINT</b>

The portion of <i>iWorkTotal</i> that has been completed so far.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The <i>iWorkTotal</i> and <i>iWorkSoFar</i> values are "points" or estimates of the amount of work to be done, and how much is completed. They are not specified in any particular units, but should be roughly proportional to how much time the total process takes. For example, to copy one small file might be considered two points, and a large file might be considered ten points. If a process is performing an operation that copies five small files and one large file, and the process has completed four of the small files, <i>iWorkSoFar</i> would be eight points (4 x 2 = 8) and <i>iWorkTotal</i> would be twenty points (5 x 2 + 10 = 20), so the estimate would be 8 of 20 points (or 40%) complete.

