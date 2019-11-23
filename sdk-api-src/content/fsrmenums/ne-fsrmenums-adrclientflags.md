---
UID: NE:fsrmenums._AdrClientFlags
title: AdrClientFlags (fsrmenums.h)

description: Enumerates flags for indicating why an access denied remediation (ADR) client operation could not be performed.
old-location: fsrm\adrclientflags.htm
tech.root: fsrm
ms.assetid: 8475e157-8757-4ace-909b-2e9030af6ad7

ms.date: 12/05/2018
ms.keywords: AdrClientFlags, AdrClientFlags enumeration [File Server Resource Manager], AdrClientFlags_FailForLocalPaths, AdrClientFlags_FailIfNotDomainJoined, AdrClientFlags_FailIfNotSupportedByServer, AdrClientFlags_None, fs.adrclientflags, fsrm.adrclientflags, fsrmenums/AdrClientFlags, fsrmenums/AdrClientFlags_FailForLocalPaths, fsrmenums/AdrClientFlags_FailIfNotDomainJoined, fsrmenums/AdrClientFlags_FailIfNotSupportedByServer, fsrmenums/AdrClientFlags_None
ms.topic: enum
f1_keywords: 
 - "fsrmenums/AdrClientFlags"
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
 - AdrClientFlags
targetos: Windows
req.typenames: AdrClientFlags
req.redist: 
ms.custom: 19H1
---

# AdrClientFlags enumeration


## -description


Enumerates flags for indicating why an access denied remediation (ADR) client operation could not be 
    performed.


## -enum-fields




### -field AdrClientFlags_None

No ADR client flags are specified.


### -field AdrClientFlags_FailForLocalPaths

ADR client operations should fail when local paths are specified.


### -field AdrClientFlags_FailIfNotSupportedByServer

ADR client operations should fail if the operation is not supported by the server.


### -field AdrClientFlags_FailIfNotDomainJoined

ADR client operations should fail if the computer is not joined to a domain.


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fsrm/fsrm-enumerations">FSRM Enumerations</a>
 

 

