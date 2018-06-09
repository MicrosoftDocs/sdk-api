---
UID: NE:fsrmenums._FsrmFileManagementType
title: "_FsrmFileManagementType"
author: windows-sdk-content
description: Defines the file management job types.
old-location: fsrm\fsrmfilemanagementtype.htm
old-project: Fsrm
ms.assetid: f4e352c7-32fe-4a42-9d64-604c29680d7d
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: FsrmFileManagementType, FsrmFileManagementType enumeration [File Server Resource Manager], FsrmFileManagementType_Custom, FsrmFileManagementType_Expiration, FsrmFileManagementType_Rms, FsrmFileManagementType_Unknown, _FsrmFileManagementType, fs.fsrmfilemanagementtype, fsrm.fsrmfilemanagementtype, fsrm/FsrmFileManagementType, fsrm/FsrmFileManagementType_Custom, fsrm/FsrmFileManagementType_Expiration, fsrm/FsrmFileManagementType_Rms, fsrm/FsrmFileManagementType_Unknown
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: fsrmenums.h
req.include-header: FsrmPipeline.h, FsrmQuota.h, FsrmReports.h, FsrmScreen.h, Fsrmenums.h
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 R2
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: FsrmEnums.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: FsrmFileManagementType
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Fsrm.h
api_name:
 - FsrmFileManagementType
product: Windows
targetos: Windows
req.lib: 
req.dll: SrmSvc.dll
req.irql: 
req.product: Internet Explorer 5
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
 

 

