---
UID: NF:fsrmscreen.IFsrmFileScreenManager.GetFileScreenException
title: IFsrmFileScreenManager::GetFileScreenException (fsrmscreen.h)
author: windows-sdk-content
description: Retrieves the specified file screen exception.
old-location: fsrm\ifsrmfilescreenmanager_getfilescreenexception.htm
tech.root: fsrm
ms.assetid: 634c54b0-2766-4248-8a27-506eaa3d6a68
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: FsrmFileScreenManager class [File Server Resource Manager],GetFileScreenException method, GetFileScreenException, GetFileScreenException method [File Server Resource Manager], GetFileScreenException method [File Server Resource Manager],FsrmFileScreenManager class, GetFileScreenException method [File Server Resource Manager],IFsrmFileScreenManager interface, IFsrmFileScreenManager interface [File Server Resource Manager],GetFileScreenException method, IFsrmFileScreenManager.GetFileScreenException, IFsrmFileScreenManager::GetFileScreenException, fs.ifsrmfilescreenmanager_getfilescreenexception, fsrm.ifsrmfilescreenmanager_getfilescreenexception, fsrmscreen/IFsrmFileScreenManager::GetFileScreenException
ms.topic: method
f1_keywords: ["fsrmscreen/IFsrmFileScreenManager.GetFileScreenException"]
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
 - IFsrmFileScreenManager.GetFileScreenException
 - FsrmFileScreenManager.GetFileScreenException
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IFsrmFileScreenManager::GetFileScreenException


## -description


Retrieves the specified file screen exception.


## -parameters




### -param path [in]

The local directory path associated with the file screen exception that you want to retrieve. The path is limited to 260 characters.


### -param fileScreenException [out]

An <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmscreen/nn-fsrmscreen-ifsrmfilescreenexception">IFsrmFileScreenException</a> interface to the file screen exception.


## -returns



The method returns the following return values.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fsrm/fsrmfilescreenmanager">FsrmFileScreenManager</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmscreen/nn-fsrmscreen-ifsrmfilescreenmanager">IFsrmFileScreenManager</a>
 

 

