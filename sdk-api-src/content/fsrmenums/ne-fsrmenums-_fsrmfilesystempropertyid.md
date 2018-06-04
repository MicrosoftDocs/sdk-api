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

# _FsrmFileSystemPropertyId enumeration


## -description


Defines the possible types of file system property ids.


## -enum-fields




### -field FsrmFileSystemPropertyId_Undefined

The file system property id is not used. This is the default.


### -field FsrmFileSystemPropertyId_FileName

The file system property id is the filename, including the extension.


### -field FsrmFileSystemPropertyId_DateCreated

The file system property id is the file's creation time.


### -field FsrmFileSystemPropertyId_DateLastAccessed

The file system property id is the file's last accessed time.


### -field FsrmFileSystemPropertyId_DateLastModified

The file system property id is the file's last modified time.


### -field FsrmFileSystemPropertyId_DateNow

The file system property id is the current time.


## -see-also




<a href="https://msdn.microsoft.com/93fdf667-8959-40a9-a374-c54ed73bbe89">FSRM Enumerations</a>



<a href="https://msdn.microsoft.com/29f19f5e-5e33-41e5-8332-4634613b2bf4">IFsrmFileConditionProperty.PropertyId</a>
 

 

