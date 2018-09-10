---
UID: NF:cscobj.IOfflineFilesSuspend.SuspendRoot
title: IOfflineFilesSuspend::SuspendRoot
author: windows-sdk-content
description: Suspend or release a share root or directory tree.
old-location: of\iofflinefilessuspend_suspendroot.htm
tech.root: offlinefiles
ms.assetid: 5307bc8c-e6e9-4ae7-b2da-036fc9c5c08d
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IOfflineFilesSuspend interface [Offline Files],SuspendRoot method, IOfflineFilesSuspend.SuspendRoot, IOfflineFilesSuspend::SuspendRoot, SuspendRoot, SuspendRoot method [Offline Files], SuspendRoot method [Offline Files],IOfflineFilesSuspend interface, cscobj/IOfflineFilesSuspend::SuspendRoot, of.iofflinefilessuspend_suspendroot
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: cscobj.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: CscSvc.dll; CscObj.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - CscSvc.dll
 - CscObj.dll
api_name:
 - IOfflineFilesSuspend.SuspendRoot
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IOfflineFilesSuspend::SuspendRoot


## -description


Suspend or release a share root or directory tree.  A suspended item  is always in the offline state and is excluded from automatic synchronization by Offline Files.


## -parameters




### -param bSuspend [in]

Specify <b>TRUE</b> to suspend, or <b>FALSE</b> to release.


## -returns



Returns <b>S_OK</b> if successful, or an error value otherwise.




## -remarks



When a share root or directory tree is suspended, all directories and files contained in the share or directory or in any subfolders are suspended as well.  This means that both directories and files may be suspended. Note that a directory can be suspended directly (if it is the root of the share or directory tree) or indirectly (if it is one of the items contained in the share or directory tree).




## -see-also




<a href="https://msdn.microsoft.com/697018c4-7cce-480a-b078-993cdac32bf5">IOfflineFilesSuspend</a>
 

 

