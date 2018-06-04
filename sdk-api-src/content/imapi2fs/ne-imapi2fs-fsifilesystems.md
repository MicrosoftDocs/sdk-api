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

# FsiFileSystems enumeration


## -description


Defines values for recognized file systems.


## -enum-fields




### -field FsiFileSystemNone

The disc does not contain a recognized file system.


### -field FsiFileSystemISO9660

Standard CD file system.


### -field FsiFileSystemJoliet

Joliet file system.


### -field FsiFileSystemUDF

UDF file system.


### -field FsiFileSystemUnknown

The disc appears to have a file system, but the layout does not match any of the recognized types.


## -see-also




<a href="https://msdn.microsoft.com/381be283-c877-44f0-9d96-b9e80a6aeec8">IFileSystemImage::IdentifyFileSystemsOnDisc</a>
 

 

