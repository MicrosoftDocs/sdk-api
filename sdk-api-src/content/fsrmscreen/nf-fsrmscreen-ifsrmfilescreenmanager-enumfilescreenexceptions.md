---
UID: NF:fsrmscreen.IFsrmFileScreenManager.EnumFileScreenExceptions
title: IFsrmFileScreenManager::EnumFileScreenExceptions (fsrmscreen.h)
description: Enumerates the file screen exceptions for the specified directory and its subdirectories.
helpviewer_keywords: ["EnumFileScreenExceptions","EnumFileScreenExceptions method [File Server Resource Manager]","EnumFileScreenExceptions method [File Server Resource Manager]","FsrmFileScreenManager class","EnumFileScreenExceptions method [File Server Resource Manager]","IFsrmFileScreenManager interface","FsrmFileScreenManager class [File Server Resource Manager]","EnumFileScreenExceptions method","IFsrmFileScreenManager interface [File Server Resource Manager]","EnumFileScreenExceptions method","IFsrmFileScreenManager.EnumFileScreenExceptions","IFsrmFileScreenManager::EnumFileScreenExceptions","fs.ifsrmfilescreenmanager_enumfilescreenexceptions","fsrm.ifsrmfilescreenmanager_enumfilescreenexceptions","fsrmscreen/IFsrmFileScreenManager::EnumFileScreenExceptions"]
old-location: fsrm\ifsrmfilescreenmanager_enumfilescreenexceptions.htm
tech.root: fsrm
ms.assetid: c30377c8-d3a3-40fe-a42c-9b36d2a0b35e
ms.date: 12/05/2018
ms.keywords: EnumFileScreenExceptions, EnumFileScreenExceptions method [File Server Resource Manager], EnumFileScreenExceptions method [File Server Resource Manager],FsrmFileScreenManager class, EnumFileScreenExceptions method [File Server Resource Manager],IFsrmFileScreenManager interface, FsrmFileScreenManager class [File Server Resource Manager],EnumFileScreenExceptions method, IFsrmFileScreenManager interface [File Server Resource Manager],EnumFileScreenExceptions method, IFsrmFileScreenManager.EnumFileScreenExceptions, IFsrmFileScreenManager::EnumFileScreenExceptions, fs.ifsrmfilescreenmanager_enumfilescreenexceptions, fsrm.ifsrmfilescreenmanager_enumfilescreenexceptions, fsrmscreen/IFsrmFileScreenManager::EnumFileScreenExceptions
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
 - IFsrmFileScreenManager::EnumFileScreenExceptions
 - fsrmscreen/IFsrmFileScreenManager::EnumFileScreenExceptions
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
 - IFsrmFileScreenManager.EnumFileScreenExceptions
 - FsrmFileScreenManager.EnumFileScreenExceptions
---

# IFsrmFileScreenManager::EnumFileScreenExceptions


## -description

Enumerates the file screen exceptions for the specified directory and its subdirectories.

## -parameters

### -param path [in]

The local directory path associated with the file screen exception that you want to retrieve.

If the path ends with "\*", retrieve all exceptions associated with the immediate subdirectories of the path (does not include the exceptions associated with the path).

If the path ends with "\...", retrieve the exception for the path and all exceptions associated with the immediate subdirectories of the path (recursively).

If the path does not end in "\*" or "\...", retrieve the exception for the path only.

If path is null or empty, the method returns all file screen exceptions.

### -param options [in]

The options to use when enumerating the exceptions. For possible values, see the <a href="/windows/desktop/api/fsrmenums/ne-fsrmenums-fsrmenumoptions">FsrmEnumOptions</a> enumeration.

### -param fileScreenExceptions [out]

An <a href="/previous-versions/windows/desktop/api/fsrm/nn-fsrm-ifsrmcommittablecollection">IFsrmCommittableCollection</a> interface that contains a collection of file screen exceptions.

Each item of the collection is a <b>VARIANT</b> of type <b>VT_DISPATCH</b>. Query the <b>pdispVal</b> member of the variant for the <a href="/previous-versions/windows/desktop/api/fsrmscreen/nn-fsrmscreen-ifsrmfilescreenexception">IFsrmFileScreenException</a> interface.

The collection contains only committed exceptions; the collection will not contain newly created exceptions that have not been committed.

The collection is empty if the path does not contain file screen exceptions.

## -returns

The method returns the following return values.

## -see-also

<a href="/previous-versions/windows/desktop/fsrm/fsrmfilescreenmanager">FsrmFileScreenManager</a>



<a href="/previous-versions/windows/desktop/api/fsrmscreen/nn-fsrmscreen-ifsrmfilescreenmanager">IFsrmFileScreenManager</a>