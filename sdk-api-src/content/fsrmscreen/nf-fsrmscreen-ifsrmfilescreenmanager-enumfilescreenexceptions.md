---
UID: NF:fsrmscreen.IFsrmFileScreenManager.EnumFileScreenExceptions
title: IFsrmFileScreenManager::EnumFileScreenExceptions
author: windows-sdk-content
description: Enumerates the file screen exceptions for the specified directory and its subdirectories.
old-location: fsrm\ifsrmfilescreenmanager_enumfilescreenexceptions.htm
tech.root: fsrm
ms.assetid: c30377c8-d3a3-40fe-a42c-9b36d2a0b35e
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: EnumFileScreenExceptions, EnumFileScreenExceptions method [File Server Resource Manager], EnumFileScreenExceptions method [File Server Resource Manager],FsrmFileScreenManager class, EnumFileScreenExceptions method [File Server Resource Manager],IFsrmFileScreenManager interface, FsrmFileScreenManager class [File Server Resource Manager],EnumFileScreenExceptions method, IFsrmFileScreenManager interface [File Server Resource Manager],EnumFileScreenExceptions method, IFsrmFileScreenManager.EnumFileScreenExceptions, IFsrmFileScreenManager::EnumFileScreenExceptions, fs.ifsrmfilescreenmanager_enumfilescreenexceptions, fsrm.ifsrmfilescreenmanager_enumfilescreenexceptions, fsrmscreen/IFsrmFileScreenManager::EnumFileScreenExceptions
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
 - IFsrmFileScreenManager.EnumFileScreenExceptions
 - FsrmFileScreenManager.EnumFileScreenExceptions
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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

The options to use when enumerating the exceptions. For possible values, see the <a href="https://msdn.microsoft.com/9c613d0c-c49a-4010-b66f-a63c57d693f7">FsrmEnumOptions</a> enumeration.


### -param fileScreenExceptions [out]

An <a href="https://msdn.microsoft.com/ef4678b4-e6b0-4044-ba11-7a3ae01ad2c7">IFsrmCommittableCollection</a> interface that contains a collection of file screen exceptions.

Each item of the collection is a <b>VARIANT</b> of type <b>VT_DISPATCH</b>. Query the <b>pdispVal</b> member of the variant for the <a href="https://msdn.microsoft.com/188e76dd-6df6-412f-8d51-fc727075de80">IFsrmFileScreenException</a> interface.

The collection contains only committed exceptions; the collection will not contain newly created exceptions that have not been committed.

The collection is empty if the path does not contain file screen exceptions.


## -returns



The method returns the following return values.




## -see-also




<a href="https://msdn.microsoft.com/82ff65fa-2e82-4f07-bdd4-e3b01d184c16">FsrmFileScreenManager</a>



<a href="https://msdn.microsoft.com/a0cea95d-5839-41a2-91b9-da8e13030682">IFsrmFileScreenManager</a>
 

 

