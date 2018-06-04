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

# _FsrmFileManagementType enumeration


## -description


Defines the file management job types.


## -enum-fields




### -field FsrmFileManagementType_Unknown

The file management type is unknown; do not use this value.


### -field FsrmFileManagementType_Expiration

The file management job expires files meeting the specified criteria.


### -field FsrmFileManagementType_Custom

This file management job runs a custom action on files meeting the specified criteria.


### -field FsrmFileManagementType_Rms

The file management jobs runs an RMS action on files meeting the specified criteria.

<b>Windows Server 2008 R2:  </b>This enumeration value is not supported before Windows Server 2012.


## -see-also




<a href="https://msdn.microsoft.com/93fdf667-8959-40a9-a374-c54ed73bbe89">FSRM Enumerations</a>



<a href="https://msdn.microsoft.com/98816ea0-7651-42ef-8893-13c568ed859a">IFsrmFileManagementJob.OperationType</a>
 

 

