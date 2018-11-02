---
UID: NF:shobjidl_core.ITransferSource.EnterFolder
title: ITransferSource::EnterFolder
author: windows-sdk-content
description: Notifies that a folder is the destination of a file operation.
old-location: shell\ITransferSource_EnterFolder.htm
tech.root: shell
ms.assetid: de6b1b03-450f-4d48-b0f4-67e268feb36a
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: EnterFolder, EnterFolder method [Windows Shell], EnterFolder method [Windows Shell],ITransferSource interface, ITransferSource interface [Windows Shell],EnterFolder method, ITransferSource.EnterFolder, ITransferSource::EnterFolder, _shell_ITransferSource_EnterFolder, shell.ITransferSource_EnterFolder, shobjidl_core/ITransferSource::EnterFolder
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
 - ITransferSource.EnterFolder
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITransferSource::EnterFolder


## -description


Notifies that a folder is the destination of a file operation.


## -parameters




### -param psiChildFolderDest [in]

Type: <b><a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a>*</b>

A pointer to the <a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a> destination folder.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



 This method is called when beginning to process a folder or subfolder in a recursive operation. For instance, when a source folder is copied to a destination folder, method <b>ITransferSource::EnterFolder</b> should be called with <i>psiChildFolderDest</i> set to the destination folder.




## -see-also




<a href="https://msdn.microsoft.com/341966d4-f9cf-457d-97ef-8e6107544283">ITransferSource</a>



<a href="https://msdn.microsoft.com/5a546603-d409-4c8e-9fa8-892c5c4844e7">ITransferSource::Advise</a>



<a href="https://msdn.microsoft.com/c8d0b757-a103-4c18-b556-8ba4ea9b3a2d">ITransferSource::LeaveFolder</a>



<a href="https://msdn.microsoft.com/4f71134e-dfbf-40e7-b72b-c4913c876689">ITransferSource::Unadvise</a>
 

 

