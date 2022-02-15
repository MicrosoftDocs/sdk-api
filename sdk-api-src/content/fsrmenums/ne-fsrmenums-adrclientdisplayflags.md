---
UID: NE:fsrmenums._AdrClientDisplayFlags
title: AdrClientDisplayFlags (fsrmenums.h)
description: Describes the possible types of access denied remediation (ADR) client display flags.
helpviewer_keywords: ["AdrClientDisplayFlags","AdrClientDisplayFlags enumeration [File Server Resource Manager]","AdrClientDisplayFlags_AllowEmailRequests","AdrClientDisplayFlags_ShowDeviceTroubleshooting","fs.adrclientdisplayflags","fsrm.adrclientdisplayflags","fsrmenums/AdrClientDisplayFlags","fsrmenums/AdrClientDisplayFlags_AllowEmailRequests","fsrmenums/AdrClientDisplayFlags_ShowDeviceTroubleshooting"]
old-location: fsrm\adrclientdisplayflags.htm
tech.root: fsrm
ms.assetid: 939ecb44-e59b-452d-901f-72207a6ae89a
ms.date: 12/05/2018
ms.keywords: AdrClientDisplayFlags, AdrClientDisplayFlags enumeration [File Server Resource Manager], AdrClientDisplayFlags_AllowEmailRequests, AdrClientDisplayFlags_ShowDeviceTroubleshooting, fs.adrclientdisplayflags, fsrm.adrclientdisplayflags, fsrmenums/AdrClientDisplayFlags, fsrmenums/AdrClientDisplayFlags_AllowEmailRequests, fsrmenums/AdrClientDisplayFlags_ShowDeviceTroubleshooting
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
targetos: Windows
req.typenames: AdrClientDisplayFlags
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _AdrClientDisplayFlags
 - fsrmenums/_AdrClientDisplayFlags
 - AdrClientDisplayFlags
 - fsrmenums/AdrClientDisplayFlags
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - FsrmEnums.h
api_name:
 - AdrClientDisplayFlags
---

# AdrClientDisplayFlags enumeration


## -description

Describes the possible types of access denied remediation (ADR) client display flags.

## -enum-fields

### -field AdrClientDisplayFlags_AllowEmailRequests:0x1

Indicates whether to send the user an email after an ADR event.

### -field AdrClientDisplayFlags_ShowDeviceTroubleshooting:0x2

Indicates whether to show the user the offending device claims.

## -see-also

<a href="/previous-versions/windows/desktop/fsrm/fsrm-enumerations">FSRM Enumerations</a>
