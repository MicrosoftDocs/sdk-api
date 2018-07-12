---
UID: NF:shobjidl_core.IFileOperation.GetAnyOperationsAborted
title: IFileOperation::GetAnyOperationsAborted
author: windows-sdk-content
description: Gets a value that states whether any file operations initiated by a call to IFileOperation::PerformOperations were stopped before they were complete. The operations could be stopped either by user action or silently by the system.
old-location: shell\IFileOperation_GetAnyOperationsAborted.htm
old-project: shell
ms.assetid: 988f78a8-3a50-44d8-9214-7cf71be72d38
ms.author: windowssdkdev
ms.date: 06/27/2018
ms.keywords: GetAnyOperationsAborted, GetAnyOperationsAborted method [Windows Shell], GetAnyOperationsAborted method [Windows Shell],IFileOperation interface, IFileOperation interface [Windows Shell],GetAnyOperationsAborted method, IFileOperation.GetAnyOperationsAborted, IFileOperation::GetAnyOperationsAborted, _shell_IFileOperation_GetAnyOperationsAborted, shell.IFileOperation_GetAnyOperationsAborted, shobjidl_core/IFileOperation::GetAnyOperationsAborted
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - IFileOperation.GetAnyOperationsAborted
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
---

# IFileOperation::GetAnyOperationsAborted


## -description


Gets a value that states whether any file operations initiated by a call to <a href="https://msdn.microsoft.com/eceb5f0a-ad9a-4b7a-9656-c10e0420a96a">IFileOperation::PerformOperations</a> were stopped before they were complete. The operations could be stopped either by user action or silently by the system.


## -parameters




### -param pfAnyOperationsAborted [out]

Type: <b>BOOL*</b>

When this method returns, points to <b>TRUE</b> if any file operations were aborted before they were complete; otherwise, <b>FALSE</b>.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Call this method after <a href="https://msdn.microsoft.com/eceb5f0a-ad9a-4b7a-9656-c10e0420a96a">IFileOperation::PerformOperations</a> returns.

You should call <b>IFileOperation::GetAnyOperationsAborted</b> regardless of whether <a href="https://msdn.microsoft.com/eceb5f0a-ad9a-4b7a-9656-c10e0420a96a">IFileOperation::PerformOperations</a> returned a success or failure code. A success code can be returned even if the operation was stopped by the user or the system.

This method provides the same functionality as the <b>fAnyOperationsAborted</b> member of the <a href="https://msdn.microsoft.com/590d87c2-0c75-44b9-a9b5-f7c37728512b">SHFILEOPSTRUCT</a> structure used by the legacy function <a href="https://msdn.microsoft.com/7807015f-52c5-46f5-9e90-4e3e60ddf705">SHFileOperation</a>.



