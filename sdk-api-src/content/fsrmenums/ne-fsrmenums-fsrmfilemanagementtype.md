---
UID: NE:fsrmenums._FsrmFileManagementType
title: FsrmFileManagementType (fsrmenums.h)
description: Defines the file management job types.
helpviewer_keywords: ["FsrmFileManagementType","FsrmFileManagementType enumeration [File Server Resource Manager]","FsrmFileManagementType_Custom","FsrmFileManagementType_Expiration","FsrmFileManagementType_Rms","FsrmFileManagementType_Unknown","fs.fsrmfilemanagementtype","fsrm.fsrmfilemanagementtype","fsrm/FsrmFileManagementType","fsrm/FsrmFileManagementType_Custom","fsrm/FsrmFileManagementType_Expiration","fsrm/FsrmFileManagementType_Rms","fsrm/FsrmFileManagementType_Unknown"]
old-location: fsrm\fsrmfilemanagementtype.htm
tech.root: fsrm
ms.assetid: f4e352c7-32fe-4a42-9d64-604c29680d7d
ms.date: 12/05/2018
ms.keywords: FsrmFileManagementType, FsrmFileManagementType enumeration [File Server Resource Manager], FsrmFileManagementType_Custom, FsrmFileManagementType_Expiration, FsrmFileManagementType_Rms, FsrmFileManagementType_Unknown, fs.fsrmfilemanagementtype, fsrm.fsrmfilemanagementtype, fsrm/FsrmFileManagementType, fsrm/FsrmFileManagementType_Custom, fsrm/FsrmFileManagementType_Expiration, fsrm/FsrmFileManagementType_Rms, fsrm/FsrmFileManagementType_Unknown
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: FsrmFileManagementType
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _FsrmFileManagementType
 - fsrmenums/_FsrmFileManagementType
 - FsrmFileManagementType
 - fsrmenums/FsrmFileManagementType
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Fsrm.h
api_name:
 - FsrmFileManagementType
---

# FsrmFileManagementType enumeration


## -description

Defines the file management job types.

## -enum-fields

### -field FsrmFileManagementType_Unknown:0

The file management type is unknown; do not use this value.

### -field FsrmFileManagementType_Expiration:1

The file management job expires files meeting the specified criteria.

### -field FsrmFileManagementType_Custom:2

This file management job runs a custom action on files meeting the specified criteria.

### -field FsrmFileManagementType_Rms:3

The file management jobs runs an RMS action on files meeting the specified criteria.

<b>Windows Server 2008 R2:  </b>This enumeration value is not supported before Windows Server 2012.

## -see-also

<a href="/previous-versions/windows/desktop/fsrm/fsrm-enumerations">FSRM Enumerations</a>



<a href="/previous-versions/windows/desktop/api/fsrmreports/nf-fsrmreports-ifsrmfilemanagementjob-get_operationtype">IFsrmFileManagementJob.OperationType</a>
