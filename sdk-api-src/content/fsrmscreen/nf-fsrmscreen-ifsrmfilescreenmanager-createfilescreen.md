---
UID: NF:fsrmscreen.IFsrmFileScreenManager.CreateFileScreen
title: IFsrmFileScreenManager::CreateFileScreen (fsrmscreen.h)
description: Creates a file screen object.
helpviewer_keywords: ["CreateFileScreen","CreateFileScreen method [File Server Resource Manager]","CreateFileScreen method [File Server Resource Manager]","FsrmFileScreenManager class","CreateFileScreen method [File Server Resource Manager]","IFsrmFileScreenManager interface","FsrmFileScreenManager class [File Server Resource Manager]","CreateFileScreen method","IFsrmFileScreenManager interface [File Server Resource Manager]","CreateFileScreen method","IFsrmFileScreenManager.CreateFileScreen","IFsrmFileScreenManager::CreateFileScreen","fs.ifsrmfilescreenmanager_createfilescreen","fsrm.ifsrmfilescreenmanager_createfilescreen","fsrmscreen/IFsrmFileScreenManager::CreateFileScreen"]
old-location: fsrm\ifsrmfilescreenmanager_createfilescreen.htm
tech.root: fsrm
ms.assetid: 5e35c647-2b5a-486b-b8c5-0bc25bd313ad
ms.date: 12/05/2018
ms.keywords: CreateFileScreen, CreateFileScreen method [File Server Resource Manager], CreateFileScreen method [File Server Resource Manager],FsrmFileScreenManager class, CreateFileScreen method [File Server Resource Manager],IFsrmFileScreenManager interface, FsrmFileScreenManager class [File Server Resource Manager],CreateFileScreen method, IFsrmFileScreenManager interface [File Server Resource Manager],CreateFileScreen method, IFsrmFileScreenManager.CreateFileScreen, IFsrmFileScreenManager::CreateFileScreen, fs.ifsrmfilescreenmanager_createfilescreen, fsrm.ifsrmfilescreenmanager_createfilescreen, fsrmscreen/IFsrmFileScreenManager::CreateFileScreen
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
 - IFsrmFileScreenManager::CreateFileScreen
 - fsrmscreen/IFsrmFileScreenManager::CreateFileScreen
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
 - IFsrmFileScreenManager.CreateFileScreen
 - FsrmFileScreenManager.CreateFileScreen
---

# IFsrmFileScreenManager::CreateFileScreen


## -description

Creates a file screen object.

## -parameters

### -param path [in]

The local directory path to which the file screen applies. The string is limited to 260 characters.

### -param fileScreen [out]

An <a href="/previous-versions/windows/desktop/api/fsrmscreen/nn-fsrmscreen-ifsrmfilescreen">IFsrmFileScreen</a> interface of the newly created file screen. To add the file screen to FSRM, call the <a href="/previous-versions/windows/desktop/api/fsrm/nf-fsrm-ifsrmobject-commit">IFsrmFileScreen::Commit</a> method.

## -returns

The method returns the following return values.

## -remarks

The screen applies to the directory and all its subdirectories (recursively). For example, a screen on P:&#92;<i>directory</i> that blocks *.mp3 also blocks MP3 files on P:&#92;<i>directory</i>&#92;<i>subdirectory</i>.

If you create a file screen on P:&#92;<i>directory</i>&#92;<i>subdirectory</i>, the screen that you created on P:&#92;<i>directory</i> still applies to P:&#92;<i>directory</i>&#92;<i>subdirectory</i>. If you do not want the screen on P:&#92;<i>directory</i> to  apply to P:&#92;<i>directory</i>&#92;<i>subdirectory</i>, you need to create a <a href="/previous-versions/windows/desktop/api/fsrmscreen/nf-fsrmscreen-ifsrmfilescreenmanager-createfilescreenexception">file screen exception</a>.


#### Examples

For an example, see <a href="/previous-versions/windows/desktop/fsrm/defining-a-file-screen">Defining a File Screen</a>.

<div class="code"></div>

## -see-also

<a href="/previous-versions/windows/desktop/fsrm/fsrmfilescreenmanager">FsrmFileScreenManager</a>



<a href="/previous-versions/windows/desktop/api/fsrmscreen/nn-fsrmscreen-ifsrmfilescreenmanager">IFsrmFileScreenManager</a>