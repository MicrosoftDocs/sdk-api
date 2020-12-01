---
UID: NF:fsrmscreen.IFsrmFileScreenManager.GetFileScreen
title: IFsrmFileScreenManager::GetFileScreen (fsrmscreen.h)
description: Retrieves the specified file screen.
helpviewer_keywords: ["FsrmFileScreenManager class [File Server Resource Manager]","GetFileScreen method","GetFileScreen","GetFileScreen method [File Server Resource Manager]","GetFileScreen method [File Server Resource Manager]","FsrmFileScreenManager class","GetFileScreen method [File Server Resource Manager]","IFsrmFileScreenManager interface","IFsrmFileScreenManager interface [File Server Resource Manager]","GetFileScreen method","IFsrmFileScreenManager.GetFileScreen","IFsrmFileScreenManager::GetFileScreen","fs.ifsrmfilescreenmanager_getfilescreen","fsrm.ifsrmfilescreenmanager_getfilescreen","fsrmscreen/IFsrmFileScreenManager::GetFileScreen"]
old-location: fsrm\ifsrmfilescreenmanager_getfilescreen.htm
tech.root: fsrm
ms.assetid: 9af0d9a7-80a2-4cc8-a703-c1af8ac5b7c9
ms.date: 12/05/2018
ms.keywords: FsrmFileScreenManager class [File Server Resource Manager],GetFileScreen method, GetFileScreen, GetFileScreen method [File Server Resource Manager], GetFileScreen method [File Server Resource Manager],FsrmFileScreenManager class, GetFileScreen method [File Server Resource Manager],IFsrmFileScreenManager interface, IFsrmFileScreenManager interface [File Server Resource Manager],GetFileScreen method, IFsrmFileScreenManager.GetFileScreen, IFsrmFileScreenManager::GetFileScreen, fs.ifsrmfilescreenmanager_getfilescreen, fsrm.ifsrmfilescreenmanager_getfilescreen, fsrmscreen/IFsrmFileScreenManager::GetFileScreen
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IFsrmFileScreenManager::GetFileScreen
 - fsrmscreen/IFsrmFileScreenManager::GetFileScreen
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - SrmSvc.dll
api_name:
 - IFsrmFileScreenManager.GetFileScreen
 - FsrmFileScreenManager.GetFileScreen
---

# IFsrmFileScreenManager::GetFileScreen


## -description

Retrieves the specified file screen.

## -parameters

### -param path [in]

The local directory path associated with the file screen that you want to retrieve. The path is limited to 260 characters.

### -param fileScreen [out]

An <a href="/previous-versions/windows/desktop/api/fsrmscreen/nn-fsrmscreen-ifsrmfilescreen">IFsrmFileScreen</a> interface to the file screen.

## -returns

The method returns the following return values.

## -see-also

<a href="/previous-versions/windows/desktop/fsrm/fsrmfilescreenmanager">FsrmFileScreenManager</a>



<a href="/previous-versions/windows/desktop/api/fsrmscreen/nn-fsrmscreen-ifsrmfilescreenmanager">IFsrmFileScreenManager</a>