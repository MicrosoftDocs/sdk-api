---
UID: NE:vss._VSS_RESTORE_TYPE
title: VSS_RESTORE_TYPE (vss.h)
description: Used by a requester to indicate the type of restore operation it is about to perform.
helpviewer_keywords: ["*PVSS_RESTORE_TYPE","PVSS_RESTORE_TYPE","PVSS_RESTORE_TYPE enumeration pointer [VSS]","VSS_RESTORE_TYPE","VSS_RESTORE_TYPE enumeration [VSS]","VSS_RTYPE_BY_COPY","VSS_RTYPE_IMPORT","VSS_RTYPE_OTHER","VSS_RTYPE_UNDEFINED","_win32_vss_restore_type","base.vss_restore_type","vss/PVSS_RESTORE_TYPE","vss/VSS_RESTORE_TYPE","vss/VSS_RTYPE_BY_COPY","vss/VSS_RTYPE_IMPORT","vss/VSS_RTYPE_OTHER","vss/VSS_RTYPE_UNDEFINED"]
old-location: base\vss_restore_type.htm
tech.root: base
ms.assetid: 4649aee5-da45-4602-a768-eff228a8d726
ms.date: 12/05/2018
ms.keywords: '*PVSS_RESTORE_TYPE, PVSS_RESTORE_TYPE, PVSS_RESTORE_TYPE enumeration pointer [VSS], VSS_RESTORE_TYPE, VSS_RESTORE_TYPE enumeration [VSS], VSS_RTYPE_BY_COPY, VSS_RTYPE_IMPORT, VSS_RTYPE_OTHER, VSS_RTYPE_UNDEFINED, _win32_vss_restore_type, base.vss_restore_type, vss/PVSS_RESTORE_TYPE, vss/VSS_RESTORE_TYPE, vss/VSS_RTYPE_BY_COPY, vss/VSS_RTYPE_IMPORT, vss/VSS_RTYPE_OTHER, vss/VSS_RTYPE_UNDEFINED'
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: VSS_RESTORE_TYPE, *PVSS_RESTORE_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _VSS_RESTORE_TYPE
 - vss/_VSS_RESTORE_TYPE
 - PVSS_RESTORE_TYPE
 - vss/PVSS_RESTORE_TYPE
 - VSS_RESTORE_TYPE
 - vss/VSS_RESTORE_TYPE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Vss.h
api_name:
 - VSS_RESTORE_TYPE
---

# VSS_RESTORE_TYPE enumeration


## -description

The <b>VSS_RESTORE_TYPE</b> enumeration is used by a 
    requester to indicate the type of restore operation it is about to perform.

## -enum-fields

### -field VSS_RTYPE_UNDEFINED:0

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
    <a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-setrestorestate">IVssBackupComponents::SetRestoreState</a>.

A writer can retrieve the type of a restore operation by calling 
    <a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-getrestoretype">CVssWriter::GetRestoreType</a>.

## -see-also

<a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-getrestoretype">CVssWriter::GetRestoreType</a>



<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-setrestorestate">IVssBackupComponents::SetRestoreState</a>
