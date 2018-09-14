---
UID: NF:fsrmscreen.IFsrmFileGroupManager.CreateFileGroup
title: IFsrmFileGroupManager::CreateFileGroup
author: windows-sdk-content
description: Creates a file group object.
old-location: fsrm\ifsrmfilegroupmanager_createfilegroup.htm
tech.root: fsrm
ms.assetid: 7e2c3672-fbb9-4da5-9e20-25c66213843c
ms.author: windowssdkdev
ms.date: 09/07/2018
ms.keywords: CreateFileGroup, CreateFileGroup method [File Server Resource Manager], CreateFileGroup method [File Server Resource Manager],FsrmFileGroupManager class, CreateFileGroup method [File Server Resource Manager],IFsrmFileGroupManager interface, FsrmFileGroupManager class [File Server Resource Manager],CreateFileGroup method, IFsrmFileGroupManager interface [File Server Resource Manager],CreateFileGroup method, IFsrmFileGroupManager.CreateFileGroup, IFsrmFileGroupManager::CreateFileGroup, fs.ifsrmfilegroupmanager_createfilegroup, fsrm.ifsrmfilegroupmanager_createfilegroup, fsrmscreen/IFsrmFileGroupManager::CreateFileGroup
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: fsrmscreen.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
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
req.dll: SrmSvc.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - SrmSvc.dll
api_name:
 - IFsrmFileGroupManager.CreateFileGroup
 - FsrmFileGroupManager.CreateFileGroup
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFsrmFileGroupManager::CreateFileGroup


## -description


<p class="CCE_Message">[This method is supported for compatibility but it's recommended to use the 
    <a href="https://msdn.microsoft.com/1CE772FA-CE33-4900-A499-058175A7C37E">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="https://msdn.microsoft.com/c090da1e-df74-4dba-aaa0-15defa85d604">MSFT_FSRMFileGroup</a> class.]

Creates a file group object.


## -parameters




### -param fileGroup [out]

An <a href="https://msdn.microsoft.com/9b657f1c-1d59-4ba5-9af9-978ffda1a348">IFsrmFileGroup</a> interface to the new file group. To 
      add the file group to FSRM, call 
      <a href="https://msdn.microsoft.com/81c9b1db-7756-47b2-98e6-8e819d93cd0f">IFsrmFileGroup::Commit</a> method.


## -returns



The method returns the following return values.




## -see-also




<a href="https://msdn.microsoft.com/d5c9c8f0-edbe-4f34-8f34-fe9d0667926e">FsrmFileGroupManager</a>



<a href="https://msdn.microsoft.com/e0a1a3d3-f683-410d-a0d9-081cd2476d1e">IFsrmFileGroupManager</a>



<a href="https://msdn.microsoft.com/c090da1e-df74-4dba-aaa0-15defa85d604">MSFT_FSRMFileGroup</a>
 

 

