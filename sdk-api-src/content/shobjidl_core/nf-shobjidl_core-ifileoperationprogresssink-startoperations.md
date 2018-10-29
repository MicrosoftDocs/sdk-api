---
UID: NF:shobjidl_core.IFileOperationProgressSink.StartOperations
title: IFileOperationProgressSink::StartOperations
author: windows-sdk-content
description: Performs caller-implemented actions before any specific file operations are performed.
old-location: shell\IFileOperationProgressSink_StartOperations.htm
tech.root: shell
ms.assetid: 8b9e4423-ead7-44be-b960-5ee83025f42a
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: IFileOperationProgressSink interface [Windows Shell],StartOperations method, IFileOperationProgressSink.StartOperations, IFileOperationProgressSink::StartOperations, StartOperations, StartOperations method [Windows Shell], StartOperations method [Windows Shell],IFileOperationProgressSink interface, _shell_IFileOperationProgressSink_StartOperations, shell.IFileOperationProgressSink_StartOperations, shobjidl_core/IFileOperationProgressSink::StartOperations
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - IFileOperationProgressSink.StartOperations
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFileOperationProgressSink::StartOperations


## -description


Performs caller-implemented actions before any specific file operations are performed.


## -parameters






## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



<b>StartOperations</b> is the first of the <a href="https://msdn.microsoft.com/24b20e05-d8be-4060-a966-7b32d9225403">IFileOperationProgressSink</a> methods to be called after <a href="https://msdn.microsoft.com/eceb5f0a-ad9a-4b7a-9656-c10e0420a96a">PerformOperations</a>. It can be used to perform any setup or initialization that you require before the file operations begin.



