---
UID: NE:fhcfg._FH_RETENTION_TYPES
title: FH_RETENTION_TYPES (fhcfg.h)
description: Specifies under what conditions previous versions of files and folders can be deleted from a backup target.
helpviewer_keywords: ["FH_RETENTION_AGE_BASED","FH_RETENTION_DISABLED","FH_RETENTION_TYPES","FH_RETENTION_TYPES enumeration [Windows API]","FH_RETENTION_UNLIMITED","MAX_RETENTION_TYPE","fhcfg/FH_RETENTION_AGE_BASED","fhcfg/FH_RETENTION_DISABLED","fhcfg/FH_RETENTION_TYPES","fhcfg/FH_RETENTION_UNLIMITED","fhcfg/MAX_RETENTION_TYPE","winprog.fh_retention_types"]
old-location: winprog\fh_retention_types.htm
tech.root: winprog
ms.assetid: B80EC7BF-1825-462C-ACE3-5163C14EE15D
ms.date: 12/05/2018
ms.keywords: FH_RETENTION_AGE_BASED, FH_RETENTION_DISABLED, FH_RETENTION_TYPES, FH_RETENTION_TYPES enumeration [Windows API], FH_RETENTION_UNLIMITED, MAX_RETENTION_TYPE, fhcfg/FH_RETENTION_AGE_BASED, fhcfg/FH_RETENTION_DISABLED, fhcfg/FH_RETENTION_TYPES, fhcfg/FH_RETENTION_UNLIMITED, fhcfg/MAX_RETENTION_TYPE, winprog.fh_retention_types
req.header: fhcfg.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Fhcfg.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: FH_RETENTION_TYPES
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _FH_RETENTION_TYPES
 - fhcfg/_FH_RETENTION_TYPES
 - FH_RETENTION_TYPES
 - fhcfg/FH_RETENTION_TYPES
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Fhcfg.h
api_name:
 - FH_RETENTION_TYPES
---

# FH_RETENTION_TYPES enumeration


## -description

Specifies under what conditions previous versions of files and folders can be deleted from a backup target.

## -enum-fields

### -field FH_RETENTION_DISABLED:0

Previous versions are never deleted from the backup target.

### -field FH_RETENTION_UNLIMITED

The operating system can delete any previous version on an as-needed basis, unless it is the most recent version of a file that currently exists and is within the protection scope.

### -field FH_RETENTION_AGE_BASED

The operating system can delete any previous version older than the specified minimum age on as-needed basis, unless it is the most recent version of a file that  currently exists and is within the protection scope. The minimum age is specified by the <b>FH_RETENTION_AGE</b> local policy.

### -field MAX_RETENTION_TYPE

The maximum enumeration value for this enumeration. This value and all values greater than it are reserved for system use.

## -remarks

The operating system deletes previous versions from a backup target only when the target is full or when the user has initiated data retention manually by using the File History item in Control Panel.

If <b>FH_RETENTION_AGE_BASED</b> is specified and the target is large enough, it is possible for the target to contain versions that are much older than the minimum age that is specified by the <b>FH_RETENTION_AGE</b> local policy.

## -see-also

<a href="/windows/desktop/api/fhcfg/nf-fhcfg-ifhconfigmgr-getlocalpolicy">IFhConfigMgr::GetLocalPolicy</a>



<a href="/windows/desktop/api/fhcfg/nf-fhcfg-ifhconfigmgr-setlocalpolicy">IFhConfigMgr::SetLocalPolicy</a>
