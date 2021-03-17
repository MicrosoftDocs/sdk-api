---
UID: NF:fsrmscreen.IFsrmFileScreenManager.CreateFileScreenException
title: IFsrmFileScreenManager::CreateFileScreenException (fsrmscreen.h)
description: Creates a file screen exception object.
helpviewer_keywords: ["CreateFileScreenException","CreateFileScreenException method [File Server Resource Manager]","CreateFileScreenException method [File Server Resource Manager]","FsrmFileScreenManager class","CreateFileScreenException method [File Server Resource Manager]","IFsrmFileScreenManager interface","FsrmFileScreenManager class [File Server Resource Manager]","CreateFileScreenException method","IFsrmFileScreenManager interface [File Server Resource Manager]","CreateFileScreenException method","IFsrmFileScreenManager.CreateFileScreenException","IFsrmFileScreenManager::CreateFileScreenException","fs.ifsrmfilescreenmanager_createfilescreenexception","fsrm.ifsrmfilescreenmanager_createfilescreenexception","fsrmscreen/IFsrmFileScreenManager::CreateFileScreenException"]
old-location: fsrm\ifsrmfilescreenmanager_createfilescreenexception.htm
tech.root: fsrm
ms.assetid: b2a15f69-49fb-46fd-9219-aa970c9eb042
ms.date: 12/05/2018
ms.keywords: CreateFileScreenException, CreateFileScreenException method [File Server Resource Manager], CreateFileScreenException method [File Server Resource Manager],FsrmFileScreenManager class, CreateFileScreenException method [File Server Resource Manager],IFsrmFileScreenManager interface, FsrmFileScreenManager class [File Server Resource Manager],CreateFileScreenException method, IFsrmFileScreenManager interface [File Server Resource Manager],CreateFileScreenException method, IFsrmFileScreenManager.CreateFileScreenException, IFsrmFileScreenManager::CreateFileScreenException, fs.ifsrmfilescreenmanager_createfilescreenexception, fsrm.ifsrmfilescreenmanager_createfilescreenexception, fsrmscreen/IFsrmFileScreenManager::CreateFileScreenException
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
 - IFsrmFileScreenManager::CreateFileScreenException
 - fsrmscreen/IFsrmFileScreenManager::CreateFileScreenException
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
 - IFsrmFileScreenManager.CreateFileScreenException
 - FsrmFileScreenManager.CreateFileScreenException
---

# IFsrmFileScreenManager::CreateFileScreenException


## -description

Creates a file screen exception object.

## -parameters

### -param path [in]

The local directory path to which the file screen exception applies. The path is limited to 260 characters.

### -param fileScreenException [out]

An <a href="/previous-versions/windows/desktop/api/fsrmscreen/nn-fsrmscreen-ifsrmfilescreenexception">IFsrmFileScreenException</a> interface of the newly created file screen exception. To add the exception to FSRM, call <a href="/previous-versions/windows/desktop/api/fsrm/nf-fsrm-ifsrmobject-commit">IFsrmFileScreenException::Commit</a> method.

## -returns

The method returns the following return values.

## -remarks

You can use the exception to allow files to be saved in a directory when a file screen would otherwise prevent it. For example, if P:&#92;<i>directory</i> contains a file screen that blocks *.mp3, you could create an exception that allows MP3 files on P:&#92;<i>directory</i>&#92;<i>subdirectory</i>.


#### Examples

For an example, see <a href="/previous-versions/windows/desktop/fsrm/defining-a-file-screen-exception">Defining a File Screen Exception</a>.

<div class="code"></div>

## -see-also

<a href="/previous-versions/windows/desktop/fsrm/fsrmfilescreenmanager">FsrmFileScreenManager</a>



<a href="/previous-versions/windows/desktop/api/fsrmscreen/nn-fsrmscreen-ifsrmfilescreenmanager">IFsrmFileScreenManager</a>