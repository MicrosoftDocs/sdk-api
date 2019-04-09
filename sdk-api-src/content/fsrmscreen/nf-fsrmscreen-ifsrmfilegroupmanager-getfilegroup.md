---
UID: NF:fsrmscreen.IFsrmFileGroupManager.GetFileGroup
title: IFsrmFileGroupManager::GetFileGroup (fsrmscreen.h)
author: windows-sdk-content
description: Retrieves the specified file group from FSRM.
old-location: fsrm\ifsrmfilegroupmanager_getfilegroup.htm
tech.root: fsrm
ms.assetid: 14b61b2b-a20e-4895-bfbe-40e9dfe0c496
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: FsrmFileGroupManager class [File Server Resource Manager],GetFileGroup method, GetFileGroup, GetFileGroup method [File Server Resource Manager], GetFileGroup method [File Server Resource Manager],FsrmFileGroupManager class, GetFileGroup method [File Server Resource Manager],IFsrmFileGroupManager interface, IFsrmFileGroupManager interface [File Server Resource Manager],GetFileGroup method, IFsrmFileGroupManager.GetFileGroup, IFsrmFileGroupManager::GetFileGroup, fs.ifsrmfilegroupmanager_getfilegroup, fsrm.ifsrmfilegroupmanager_getfilegroup, fsrmscreen/IFsrmFileGroupManager::GetFileGroup
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
 - IFsrmFileGroupManager.GetFileGroup
 - FsrmFileGroupManager.GetFileGroup
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFsrmFileGroupManager::GetFileGroup


## -description


<p class="CCE_Message">[This method is supported for compatibility but it's recommended to use the 
    <a href="https://msdn.microsoft.com/1CE772FA-CE33-4900-A499-058175A7C37E">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="https://msdn.microsoft.com/c090da1e-df74-4dba-aaa0-15defa85d604">MSFT_FSRMFileGroup</a> class.]

Retrieves the specified file group from FSRM.


## -parameters




### -param name [in]

The name of the file group to retrieve. The string is limited to 4,000 characters.


### -param fileGroup [out]

An <a href="https://msdn.microsoft.com/9b657f1c-1d59-4ba5-9af9-978ffda1a348">IFsrmFileGroup</a> interface to the retrieved file 
      group.


## -returns



The method returns the following return values.




## -see-also




<a href="https://msdn.microsoft.com/d5c9c8f0-edbe-4f34-8f34-fe9d0667926e">FsrmFileGroupManager</a>



<a href="https://msdn.microsoft.com/e0a1a3d3-f683-410d-a0d9-081cd2476d1e">IFsrmFileGroupManager</a>



<a href="https://msdn.microsoft.com/c090da1e-df74-4dba-aaa0-15defa85d604">MSFT_FSRMFileGroup</a>
 

 

