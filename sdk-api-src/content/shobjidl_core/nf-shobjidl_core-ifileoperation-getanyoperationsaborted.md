---
UID: NF:shobjidl_core.IFileOperation.GetAnyOperationsAborted
title: IFileOperation::GetAnyOperationsAborted (shobjidl_core.h)
description: Gets a value that states whether any file operations initiated by a call to IFileOperation::PerformOperations were stopped before they were complete. The operations could be stopped either by user action or silently by the system.
helpviewer_keywords: ["GetAnyOperationsAborted","GetAnyOperationsAborted method [Windows Shell]","GetAnyOperationsAborted method [Windows Shell]","IFileOperation interface","IFileOperation interface [Windows Shell]","GetAnyOperationsAborted method","IFileOperation.GetAnyOperationsAborted","IFileOperation::GetAnyOperationsAborted","_shell_IFileOperation_GetAnyOperationsAborted","shell.IFileOperation_GetAnyOperationsAborted","shobjidl_core/IFileOperation::GetAnyOperationsAborted"]
old-location: shell\IFileOperation_GetAnyOperationsAborted.htm
tech.root: shell
ms.assetid: 988f78a8-3a50-44d8-9214-7cf71be72d38
ms.date: 12/05/2018
ms.keywords: GetAnyOperationsAborted, GetAnyOperationsAborted method [Windows Shell], GetAnyOperationsAborted method [Windows Shell],IFileOperation interface, IFileOperation interface [Windows Shell],GetAnyOperationsAborted method, IFileOperation.GetAnyOperationsAborted, IFileOperation::GetAnyOperationsAborted, _shell_IFileOperation_GetAnyOperationsAborted, shell.IFileOperation_GetAnyOperationsAborted, shobjidl_core/IFileOperation::GetAnyOperationsAborted
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
 - IFileOperation::GetAnyOperationsAborted
 - shobjidl_core/IFileOperation::GetAnyOperationsAborted
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
 - IFileOperation.GetAnyOperationsAborted
---

# IFileOperation::GetAnyOperationsAborted


## -description

Gets a value that states whether any file operations initiated by a call to <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifileoperation-performoperations">IFileOperation::PerformOperations</a> were stopped before they were complete. The operations could be stopped either by user action or silently by the system.

## -parameters

### -param pfAnyOperationsAborted [out]

Type: <b>BOOL*</b>

When this method returns, points to <b>TRUE</b> if any file operations were aborted before they were complete; otherwise, <b>FALSE</b>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Call this method after <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifileoperation-performoperations">IFileOperation::PerformOperations</a> returns.

You should call <b>IFileOperation::GetAnyOperationsAborted</b> regardless of whether <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifileoperation-performoperations">IFileOperation::PerformOperations</a> returned a success or failure code. A success code can be returned even if the operation was stopped by the user or the system.

This method provides the same functionality as the <b>fAnyOperationsAborted</b> member of the <a href="/windows/desktop/api/shellapi/ns-shellapi-shfileopstructa">SHFILEOPSTRUCT</a> structure used by the legacy function <a href="/windows/desktop/api/shellapi/nf-shellapi-shfileoperationa">SHFileOperation</a>.