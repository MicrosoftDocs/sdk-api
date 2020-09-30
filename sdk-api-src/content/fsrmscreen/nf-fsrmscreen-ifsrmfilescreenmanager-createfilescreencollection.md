---
UID: NF:fsrmscreen.IFsrmFileScreenManager.CreateFileScreenCollection
title: IFsrmFileScreenManager::CreateFileScreenCollection (fsrmscreen.h)
description: Creates an empty collection to which you can add file screens.
helpviewer_keywords: ["CreateFileScreenCollection","CreateFileScreenCollection method [File Server Resource Manager]","CreateFileScreenCollection method [File Server Resource Manager]","FsrmFileScreenManager class","CreateFileScreenCollection method [File Server Resource Manager]","IFsrmFileScreenManager interface","FsrmFileScreenManager class [File Server Resource Manager]","CreateFileScreenCollection method","IFsrmFileScreenManager interface [File Server Resource Manager]","CreateFileScreenCollection method","IFsrmFileScreenManager.CreateFileScreenCollection","IFsrmFileScreenManager::CreateFileScreenCollection","fs.ifsrmfilescreenmanager_createfilescreencollection","fsrm.ifsrmfilescreenmanager_createfilescreencollection","fsrmscreen/IFsrmFileScreenManager::CreateFileScreenCollection"]
old-location: fsrm\ifsrmfilescreenmanager_createfilescreencollection.htm
tech.root: fsrm
ms.assetid: 4adce5d6-8be6-477b-8dab-d437163b4449
ms.date: 12/05/2018
ms.keywords: CreateFileScreenCollection, CreateFileScreenCollection method [File Server Resource Manager], CreateFileScreenCollection method [File Server Resource Manager],FsrmFileScreenManager class, CreateFileScreenCollection method [File Server Resource Manager],IFsrmFileScreenManager interface, FsrmFileScreenManager class [File Server Resource Manager],CreateFileScreenCollection method, IFsrmFileScreenManager interface [File Server Resource Manager],CreateFileScreenCollection method, IFsrmFileScreenManager.CreateFileScreenCollection, IFsrmFileScreenManager::CreateFileScreenCollection, fs.ifsrmfilescreenmanager_createfilescreencollection, fsrm.ifsrmfilescreenmanager_createfilescreencollection, fsrmscreen/IFsrmFileScreenManager::CreateFileScreenCollection
req.header: fsrmscreen.h
req.include-header: FsrmQuota.h
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
 - IFsrmFileScreenManager::CreateFileScreenCollection
 - fsrmscreen/IFsrmFileScreenManager::CreateFileScreenCollection
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
 - IFsrmFileScreenManager.CreateFileScreenCollection
 - FsrmFileScreenManager.CreateFileScreenCollection
---

# IFsrmFileScreenManager::CreateFileScreenCollection


## -description

Creates an empty collection to which you can add file screens.

## -parameters

### -param collection [out]

An <a href="/previous-versions/windows/desktop/api/fsrm/nn-fsrm-ifsrmcommittablecollection">IFsrmCommittableCollection</a> interface to the newly created collection. To add an object to the collection, call the <a href="/previous-versions/windows/desktop/api/fsrm/nf-fsrm-ifsrmmutablecollection-add">IFsrmMutableCollection::Add</a> method.

## -returns

The method returns the following return values.

## -remarks

After adding the file screens to the collection, call the <a href="/previous-versions/windows/desktop/api/fsrm/nf-fsrm-ifsrmcommittablecollection-commit">IFsrmCommittableCollection::Commit</a> method.

## -see-also

<a href="/previous-versions/windows/desktop/fsrm/fsrmfilescreenmanager">FsrmFileScreenManager</a>



<a href="/previous-versions/windows/desktop/api/fsrmscreen/nn-fsrmscreen-ifsrmfilescreenmanager">IFsrmFileScreenManager</a>