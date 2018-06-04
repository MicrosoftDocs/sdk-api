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

# _VSS_RESTORE_TYPE enumeration


## -description


The <b>VSS_RESTORE_TYPE</b> enumeration is used by a 
    requester to indicate the type of restore operation it is about to perform.


## -enum-fields




### -field VSS_RTYPE_UNDEFINED

No restore type is defined. 
      This is the default restore type. However, writers should treat this restore type as if it were VSS_RTYPE_BY_COPY.

This indicates an error on the part of the requester.


### -field VSS_RTYPE_BY_COPY

A requester restores backed-up data to the original volume from a backup 
      medium.


### -field VSS_RTYPE_IMPORT

A requester does not copy data from a backup medium, but imports a transportable shadow copy and uses this 
      imported volume for operations such as data mining. 
      

<b>Windows Server 2003, Standard Edition and Windows Server 2003, Web Edition:  </b>This value is not supported. All editions of Windows Server 2003 with SP1 support this value.


### -field VSS_RTYPE_OTHER

A restore type not currently enumerated. This value indicates an application error.


## -remarks



A requester can optionally set the type of a restore operation using 
    <a href="https://msdn.microsoft.com/bc85e93f-1034-41cc-bf69-025aa86a56fd">IVssBackupComponents::SetRestoreState</a>.

A writer can retrieve the type of a restore operation by calling 
    <a href="https://msdn.microsoft.com/438298ee-ab8b-4604-9d43-5acefd7cabd5">CVssWriter::GetRestoreType</a>.




## -see-also




<a href="https://msdn.microsoft.com/438298ee-ab8b-4604-9d43-5acefd7cabd5">CVssWriter::GetRestoreType</a>



<a href="https://msdn.microsoft.com/bc85e93f-1034-41cc-bf69-025aa86a56fd">IVssBackupComponents::SetRestoreState</a>
 

 

