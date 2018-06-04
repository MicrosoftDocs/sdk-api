---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# _FsrmStorageModuleCaps enumeration


## -description


Flags that define the capabilities of the storage module.


## -enum-fields




### -field FsrmStorageModuleCaps_Unknown

The storage module's capabilities are unknown. Do not use this value.


### -field FsrmStorageModuleCaps_CanGet

The storage module is allowed to retrieve classification properties.


### -field FsrmStorageModuleCaps_CanSet

The storage module is allowed to store classification properties.


### -field FsrmStorageModuleCaps_CanHandleDirectories

The storage module is allowed to handle folders. Only secure properties 
       (<b>FsrmPropertyDefinitionFlags_Secure</b> flags set on the 
       <a href="https://msdn.microsoft.com/35eb6597-b358-4084-99dc-931bad8a4425">PropertyDefinitionFlags</a> 
       property) can be stored unless <b>FsrmStorageModuleCaps_CanHandleFiles</b> is also 
       specified.

<b>Windows Server 2008 R2:  </b>This storage module capability is not supported before Windows Server 2012.


### -field FsrmStorageModuleCaps_CanHandleFiles

The storage module is allowed to handle files.

<b>Windows Server 2008 R2:  </b>This storage module capability is not supported before Windows Server 2012.


## -see-also




<a href="https://msdn.microsoft.com/94e8a6fa-11f7-4ba4-a02b-c62c5f017b8a">IFsrmStorageModuleDefinition.Capabilities</a>
 

 

