---
UID: NE:fsrmenums._AdrEmailFlags
title: AdrEmailFlags (fsrmenums.h)
description: Describes the options for access denied remediation (ADR) email.
helpviewer_keywords: ["AdrEmailFlags","AdrEmailFlags enumeration [File Server Resource Manager]","AdrEmailFlags_GenerateEventLog","AdrEmailFlags_IncludeDeviceClaims","AdrEmailFlags_IncludeUserInfo","AdrEmailFlags_PutAdminOnToLine","AdrEmailFlags_PutDataOwnerOnToLine","fs.adremailflags","fsrm.adremailflags","fsrmenums/AdrEmailFlags","fsrmenums/AdrEmailFlags_GenerateEventLog","fsrmenums/AdrEmailFlags_IncludeDeviceClaims","fsrmenums/AdrEmailFlags_IncludeUserInfo","fsrmenums/AdrEmailFlags_PutAdminOnToLine","fsrmenums/AdrEmailFlags_PutDataOwnerOnToLine"]
old-location: fsrm\adremailflags.htm
tech.root: fsrm
ms.assetid: 149c0f4b-b30b-4439-b8a8-d0423be41c64
ms.date: 12/05/2018
ms.keywords: AdrEmailFlags, AdrEmailFlags enumeration [File Server Resource Manager], AdrEmailFlags_GenerateEventLog, AdrEmailFlags_IncludeDeviceClaims, AdrEmailFlags_IncludeUserInfo, AdrEmailFlags_PutAdminOnToLine, AdrEmailFlags_PutDataOwnerOnToLine, fs.adremailflags, fsrm.adremailflags, fsrmenums/AdrEmailFlags, fsrmenums/AdrEmailFlags_GenerateEventLog, fsrmenums/AdrEmailFlags_IncludeDeviceClaims, fsrmenums/AdrEmailFlags_IncludeUserInfo, fsrmenums/AdrEmailFlags_PutAdminOnToLine, fsrmenums/AdrEmailFlags_PutDataOwnerOnToLine
f1_keywords:
- fsrmenums/AdrEmailFlags
dev_langs:
- c++
req.header: fsrmenums.h
req.include-header: FsrmPipeline.h, FsrmQuota.h, FsrmReports.h, FsrmScreen.h
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2012
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
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- FsrmEnums.h
api_name:
- AdrEmailFlags
targetos: Windows
req.typenames: AdrEmailFlags
req.redist: 
ms.custom: 19H1
---

# AdrEmailFlags enumeration


## -description


Describes the options for access denied remediation (ADR) email.


## -enum-fields




### -field AdrEmailFlags_PutDataOwnerOnToLine

The ADR email will include the owner on the To: line.


### -field AdrEmailFlags_PutAdminOnToLine

The ADR email will include the administrator on the To: line.


### -field AdrEmailFlags_IncludeDeviceClaims

The ADR email will include the device claims.


### -field AdrEmailFlags_IncludeUserInfo

The ADR email will include the user information.


### -field AdrEmailFlags_GenerateEventLog

When the ADR email is sent, an entry will be added to the event log.


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fsrm/fsrm-enumerations">FSRM Enumerations</a>
 

 

