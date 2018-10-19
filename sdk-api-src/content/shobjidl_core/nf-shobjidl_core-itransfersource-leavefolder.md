---
UID: NF:shobjidl_core.ITransferSource.LeaveFolder
title: ITransferSource::LeaveFolder
author: windows-sdk-content
description: Sends notification that a folder is no longer the destination of a file operation.
old-location: shell\ITransferSource_LeaveFolder.htm
tech.root: shell
ms.assetid: c8d0b757-a103-4c18-b556-8ba4ea9b3a2d
ms.author: windowssdkdev
ms.date: 10/18/2018
ms.keywords: ITransferSource interface [Windows Shell],LeaveFolder method, ITransferSource.LeaveFolder, ITransferSource::LeaveFolder, LeaveFolder, LeaveFolder method [Windows Shell], LeaveFolder method [Windows Shell],ITransferSource interface, _shell_ITransferSource_LeaveFolder, shell.ITransferSource_LeaveFolder, shobjidl_core/ITransferSource::LeaveFolder
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
 - ITransferSource.LeaveFolder
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITransferSource::LeaveFolder


## -description


Sends notification that a folder is no longer the destination of a file operation.


## -parameters




### -param psiChildFolderDest [in]

Type: <b><a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a>*</b>

A pointer to the <a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a> destination folder.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method is called at the end of recursive file operations on a destination folder.




## -see-also




<a href="https://msdn.microsoft.com/341966d4-f9cf-457d-97ef-8e6107544283">ITransferSource</a>



<a href="https://msdn.microsoft.com/5a546603-d409-4c8e-9fa8-892c5c4844e7">ITransferSource::Advise</a>



<a href="https://msdn.microsoft.com/de6b1b03-450f-4d48-b0f4-67e268feb36a">ITransferSource::EnterFolder</a>



<a href="https://msdn.microsoft.com/4f71134e-dfbf-40e7-b72b-c4913c876689">ITransferSource::Unadvise</a>
 

 

