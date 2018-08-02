---
UID: NE:vss._VSS_RESTORE_TYPE
title: "_VSS_RESTORE_TYPE"
author: windows-sdk-content
description: Used by a requester to indicate the type of restore operation it is about to perform.
old-location: base\vss_restore_type.htm
old-project: VSS
ms.assetid: 4649aee5-da45-4602-a768-eff228a8d726
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: "*PVSS_RESTORE_TYPE, PVSS_RESTORE_TYPE, PVSS_RESTORE_TYPE enumeration pointer [VSS], VSS_RESTORE_TYPE, VSS_RESTORE_TYPE enumeration [VSS], VSS_RTYPE_BY_COPY, VSS_RTYPE_IMPORT, VSS_RTYPE_OTHER, VSS_RTYPE_UNDEFINED, _VSS_RESTORE_TYPE, _win32_vss_restore_type, base.vss_restore_type, vss/PVSS_RESTORE_TYPE, vss/VSS_RESTORE_TYPE, vss/VSS_RTYPE_BY_COPY, vss/VSS_RTYPE_IMPORT, vss/VSS_RTYPE_OTHER, vss/VSS_RTYPE_UNDEFINED"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: vss.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: VSS_RESTORE_TYPE, *PVSS_RESTORE_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Vss.h
api_name:
 - VSS_RESTORE_TYPE
product: Windows
targetos: Windows
req.lib: VssApi.lib
req.dll: 
req.irql: 
req.product: Windows UI
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
 

 

