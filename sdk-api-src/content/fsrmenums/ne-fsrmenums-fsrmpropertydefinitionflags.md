---
UID: NE:fsrmenums._FsrmPropertyDefinitionFlags
title: FsrmPropertyDefinitionFlags (fsrmenums.h)
description: Flags the describe the type of classification property.
helpviewer_keywords: ["FsrmPropertyDefinitionFlags","FsrmPropertyDefinitionFlags enumeration [File Server Resource Manager]","FsrmPropertyDefinitionFlags_Deprecated","FsrmPropertyDefinitionFlags_Global","FsrmPropertyDefinitionFlags_Secure","fs.fsrmpropertydefinitionflags","fsrm.fsrmpropertydefinitionflags","fsrmenums/FsrmPropertyDefinitionFlags","fsrmenums/FsrmPropertyDefinitionFlags_Deprecated","fsrmenums/FsrmPropertyDefinitionFlags_Global","fsrmenums/FsrmPropertyDefinitionFlags_Secure"]
old-location: fsrm\fsrmpropertydefinitionflags.htm
tech.root: fsrm
ms.assetid: a31f2401-affa-438b-a484-7b70ea6e9181
ms.date: 12/05/2018
ms.keywords: FsrmPropertyDefinitionFlags, FsrmPropertyDefinitionFlags enumeration [File Server Resource Manager], FsrmPropertyDefinitionFlags_Deprecated, FsrmPropertyDefinitionFlags_Global, FsrmPropertyDefinitionFlags_Secure, fs.fsrmpropertydefinitionflags, fsrm.fsrmpropertydefinitionflags, fsrmenums/FsrmPropertyDefinitionFlags, fsrmenums/FsrmPropertyDefinitionFlags_Deprecated, fsrmenums/FsrmPropertyDefinitionFlags_Global, fsrmenums/FsrmPropertyDefinitionFlags_Secure
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
req.typenames: FsrmPropertyDefinitionFlags
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _FsrmPropertyDefinitionFlags
 - fsrmenums/_FsrmPropertyDefinitionFlags
 - FsrmPropertyDefinitionFlags
 - fsrmenums/FsrmPropertyDefinitionFlags
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
 - FsrmPropertyDefinitionFlags
---

# FsrmPropertyDefinitionFlags enumeration


## -description

Flags the describe the type of classification property.

## -enum-fields

### -field FsrmPropertyDefinitionFlags_Global:0x1

The FSRM classification property definition is defined globally, using group policy.

### -field FsrmPropertyDefinitionFlags_Deprecated:0x2

The FSRM classification property definition is deprecated.

### -field FsrmPropertyDefinitionFlags_Secure:0x4

The FSRM classification property definition is used for security purposes.

