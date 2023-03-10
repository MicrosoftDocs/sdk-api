---
UID: NF:fsrmscreen.IFsrmFileScreenManager.EnumFileScreens
title: IFsrmFileScreenManager::EnumFileScreens (fsrmscreen.h)
description: Enumerates the file screens for the specified directory and its subdirectories.
helpviewer_keywords: ["EnumFileScreens","EnumFileScreens method [File Server Resource Manager]","EnumFileScreens method [File Server Resource Manager]","FsrmFileScreenManager class","EnumFileScreens method [File Server Resource Manager]","IFsrmFileScreenManager interface","FsrmFileScreenManager class [File Server Resource Manager]","EnumFileScreens method","IFsrmFileScreenManager interface [File Server Resource Manager]","EnumFileScreens method","IFsrmFileScreenManager.EnumFileScreens","IFsrmFileScreenManager::EnumFileScreens","fs.ifsrmfilescreenmanager_enumfilescreens","fsrm.ifsrmfilescreenmanager_enumfilescreens","fsrmscreen/IFsrmFileScreenManager::EnumFileScreens"]
old-location: fsrm\ifsrmfilescreenmanager_enumfilescreens.htm
tech.root: fsrm
ms.assetid: 5826d5c3-885a-4001-aa89-0bc1c03b9338
ms.date: 12/05/2018
ms.keywords: EnumFileScreens, EnumFileScreens method [File Server Resource Manager], EnumFileScreens method [File Server Resource Manager],FsrmFileScreenManager class, EnumFileScreens method [File Server Resource Manager],IFsrmFileScreenManager interface, FsrmFileScreenManager class [File Server Resource Manager],EnumFileScreens method, IFsrmFileScreenManager interface [File Server Resource Manager],EnumFileScreens method, IFsrmFileScreenManager.EnumFileScreens, IFsrmFileScreenManager::EnumFileScreens, fs.ifsrmfilescreenmanager_enumfilescreens, fsrm.ifsrmfilescreenmanager_enumfilescreens, fsrmscreen/IFsrmFileScreenManager::EnumFileScreens
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
 - IFsrmFileScreenManager::EnumFileScreens
 - fsrmscreen/IFsrmFileScreenManager::EnumFileScreens
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
 - IFsrmFileScreenManager.EnumFileScreens
 - FsrmFileScreenManager.EnumFileScreens
---

# IFsrmFileScreenManager::EnumFileScreens


## -description

Enumerates the file screens for the specified directory and its subdirectories.

## -parameters

### -param path [in]

The local directory path associated with the file screen that you want to retrieve.

If the path ends with "\*", retrieve all file screens associated with the immediate subdirectories of the path (does not include the file screen associated with the path).

If the path ends with "\...", retrieve the file screen for the path and all file screens associated with the immediate subdirectories of the path (recursively).

If the path does not end in "\*" or "\...", retrieve the file screen for the path only.

If path is null or empty, the method returns all file screens.

### -param options [in]

The options to use when enumerating the file screens. For possible values, see the <a href="/windows/desktop/api/fsrmenums/ne-fsrmenums-fsrmenumoptions">FsrmEnumOptions</a> enumeration.

### -param fileScreens [out]

An <a href="/previous-versions/windows/desktop/api/fsrm/nn-fsrm-ifsrmcommittablecollection">IFsrmCommittableCollection</a> interface that contains a collection of file screens.

Each item of the collection is a <b>VARIANT</b> of type <b>VT_DISPATCH</b>. Query the <b>pdispVal</b> member of the variant for the <a href="/previous-versions/windows/desktop/api/fsrmscreen/nn-fsrmscreen-ifsrmfilescreen">IFsrmFileScreen</a> interface.

The collection contains only committed file screens; the collection will not contain newly created file screens that have not been committed.

The collection is empty if the path does not contain file screens.

## -returns

The method returns the following return values.

## -see-also

<a href="/previous-versions/windows/desktop/fsrm/fsrmfilescreenmanager">FsrmFileScreenManager</a>



<a href="/previous-versions/windows/desktop/api/fsrmscreen/nn-fsrmscreen-ifsrmfilescreenmanager">IFsrmFileScreenManager</a>