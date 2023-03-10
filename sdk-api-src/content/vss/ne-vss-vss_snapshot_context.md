---
UID: NE:vss._VSS_SNAPSHOT_CONTEXT
title: VSS_SNAPSHOT_CONTEXT (vss.h)
description: Specify how a shadow copy is to be created, queried, or deleted and the degree of writer involvement.
helpviewer_keywords: ["*PVSS_SNAPSHOT_CONTEXT","PVSS_SNAPSHOT_CONTEXT","PVSS_SNAPSHOT_CONTEXT enumeration pointer [VSS]","VSS_CTX_ALL","VSS_CTX_APP_ROLLBACK","VSS_CTX_BACKUP","VSS_CTX_CLIENT_ACCESSIBLE","VSS_CTX_CLIENT_ACCESSIBLE_WRITERS","VSS_CTX_FILE_SHARE_BACKUP","VSS_CTX_NAS_ROLLBACK","VSS_SNAPSHOT_CONTEXT","VSS_SNAPSHOT_CONTEXT enumeration [VSS]","_VSS_SNAPSHOT_CONTEXT","_VSS_SNAPSHOT_CONTEXT enumeration [VSS]","_win32__vss_snapshot_context","base._vss_snapshot_context","vss/PVSS_SNAPSHOT_CONTEXT","vss/VSS_CTX_ALL","vss/VSS_CTX_APP_ROLLBACK","vss/VSS_CTX_BACKUP","vss/VSS_CTX_CLIENT_ACCESSIBLE","vss/VSS_CTX_CLIENT_ACCESSIBLE_WRITERS","vss/VSS_CTX_FILE_SHARE_BACKUP","vss/VSS_CTX_NAS_ROLLBACK","vss/_VSS_SNAPSHOT_CONTEXT"]
old-location: base\_vss_snapshot_context.htm
tech.root: base
ms.assetid: 2efe3066-4b91-4501-bacb-4211b222e0c3
ms.date: 12/05/2018
ms.keywords: '*PVSS_SNAPSHOT_CONTEXT, PVSS_SNAPSHOT_CONTEXT, PVSS_SNAPSHOT_CONTEXT enumeration pointer [VSS], VSS_CTX_ALL, VSS_CTX_APP_ROLLBACK, VSS_CTX_BACKUP, VSS_CTX_CLIENT_ACCESSIBLE, VSS_CTX_CLIENT_ACCESSIBLE_WRITERS, VSS_CTX_FILE_SHARE_BACKUP, VSS_CTX_NAS_ROLLBACK, VSS_SNAPSHOT_CONTEXT, VSS_SNAPSHOT_CONTEXT enumeration [VSS], _VSS_SNAPSHOT_CONTEXT, _VSS_SNAPSHOT_CONTEXT enumeration [VSS], _win32__vss_snapshot_context, base._vss_snapshot_context, vss/PVSS_SNAPSHOT_CONTEXT, vss/VSS_CTX_ALL, vss/VSS_CTX_APP_ROLLBACK, vss/VSS_CTX_BACKUP, vss/VSS_CTX_CLIENT_ACCESSIBLE, vss/VSS_CTX_CLIENT_ACCESSIBLE_WRITERS, vss/VSS_CTX_FILE_SHARE_BACKUP, vss/VSS_CTX_NAS_ROLLBACK, vss/_VSS_SNAPSHOT_CONTEXT'
req.header: vss.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
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
req.typenames: VSS_SNAPSHOT_CONTEXT, *PVSS_SNAPSHOT_CONTEXT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _VSS_SNAPSHOT_CONTEXT
 - vss/_VSS_SNAPSHOT_CONTEXT
 - PVSS_SNAPSHOT_CONTEXT
 - vss/PVSS_SNAPSHOT_CONTEXT
 - VSS_SNAPSHOT_CONTEXT
 - vss/VSS_SNAPSHOT_CONTEXT
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
 - VSS_SNAPSHOT_CONTEXT
---

# VSS_SNAPSHOT_CONTEXT enumeration


## -description

The <b>_VSS_SNAPSHOT_CONTEXT</b> enumeration 
    enables a requester using 
    <a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-setcontext">IVssBackupComponents::SetContext</a> to 
    specify how a shadow copy is to be created, queried, or deleted and the degree of writer 
    involvement.

## -enum-fields

### -field VSS_CTX_BACKUP:0

The standard backup context. Specifies an auto-release, nonpersistent shadow copy in which writers are 
      involved in the creation.

### -field VSS_CTX_FILE_SHARE_BACKUP

Specifies an auto-release, nonpersistent shadow copy created without writer involvement.

### -field VSS_CTX_NAS_ROLLBACK

Specifies a persistent, non-auto-release shadow copy without writer involvement. This context should be 
      used when there is no need for writer involvement to ensure that files are in a consistent state at the time 
      of the shadow copy. 
      

Lightweight automated file rollback mechanisms or persistent shadow copies of file shares or data volumes 
       that are not expected to contain any system-related files or databases might run under this context. For 
       example, a requester could use this context for creating a shadow copy of a NAS volume hosting documents and 
       simple user shares. Those types of data do not need writer involvement to create a consistent shadow copy.

### -field VSS_CTX_APP_ROLLBACK

Specifies a persistent, non-auto-release shadow copy with writer involvement. This context is designed 
      to be used when writers are needed to ensure that files are in a well-defined state prior to shadow copy.
      

Automated file rollback mechanisms of system volumes and shadow copies to be used in data mining or restore 
       operations might run under this context. This context is similar to <b>VSS_CTX_BACKUP</b> 
       but allows a requester more control over the persistence of the shadow copy.

### -field VSS_CTX_CLIENT_ACCESSIBLE

Specifies a read-only, <a href="/windows/win32/vss/vssgloss-c">client-accessible shadow copy</a> that supports Shadow Copies for Shared Folders and is created without writer involvement. Only the system provider (the default provider available on the system) can create this type of shadow copy.

Most requesters will want to use the <b>VSS_CTX_NAS_ROLLBACK</b> context for persistent, non-auto-release shadow copies without writer involvement.

### -field VSS_CTX_CLIENT_ACCESSIBLE_WRITERS

Specifies a read-only, <a href="/windows/win32/vss/vssgloss-c">client-accessible shadow copy</a> that is created with writer involvement. Only the system provider (the default provider available on the system) can create this type of shadow copy.

Most requesters will want to use the <b>VSS_CTX_APP_ROLLBACK</b> context for persistent, non-auto-release shadow copies with writer involvement.

<b>Windows Server 2003 and Windows XP:  </b>This context is not supported by Windows Server 2003 and Windows XP.

### -field VSS_CTX_ALL:0xffffffff

All types of currently live shadow copies are available for administrative operations, such as shadow copy 
      queries (see <a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-query">IVssBackupComponents::Query</a>). 
      <b>VSS_CTX_ALL</b> is a valid context for all VSS interfaces except 
      <a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-startsnapshotset">IVssBackupComponents::StartSnapshotSet</a> 
      and 
      <a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset">IVssBackupComponents::DoSnapshotSet</a>.

## -remarks

The data type to be used with values of 
    <b>_VSS_SNAPSHOT_CONTEXT</b> is 
    <b>LONG</b>.

The default context for VSS shadow copies is <b>VSS_CTX_BACKUP</b>.

<b>Windows XP:  </b>The only supported context is the default, <b>VSS_CTX_BACKUP</b>. Calling 
     <a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-setcontext">IVssBackupComponents::SetContext</a> will 
     return <b>E_NOTIMPL</b>.

For details on how to use VSS shadow copies contexts, see 
    <a href="/windows/desktop/VSS/implementation-details-for-creating-shadow-copies">Implementation Details for 
    Creating Shadow Copies</a>.

Shadow copy behavior can be further controlled by using a bitwise OR to combine a supported 
    <a href="/windows/desktop/api/vss/ne-vss-vss_volume_snapshot_attributes">_VSS_VOLUME_SNAPSHOT_ATTRIBUTES</a> with valid 
    <b>_VSS_SNAPSHOT_CONTEXT</b> values as an argument to the 
    <a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-setcontext">IVssBackupComponents::SetContext</a> 
    method.

Currently, the only supported modifications are the bitwise OR of a 
     <b>_VSS_SNAPSHOT_CONTEXT</b> value with the
     <b>VSS_VOLSNAP_ATTR_TRANSPORTABLE</b> and either the 
     <b>VSS_VOLSNAP_ATTR_DIFFERENTIAL</b> or the <b>VSS_VOLSNAP_ATTR_PLEX</b> 
     value of the 
     <a href="/windows/desktop/api/vss/ne-vss-vss_volume_snapshot_attributes">_VSS_VOLUME_SNAPSHOT_ATTRIBUTES</a> 
     enumeration.

However, these values cannot be used to modify <b>VSS_CTX_CLIENT_ACCESSIBLE</b> 
     context.

The use of <b>VSS_VOLSNAP_ATTR_TRANSPORTABLE</b> is limited to systems running 
    Windows Server 2008 Enterprise, Windows Server 2008 Datacenter, Windows Server 2003, Enterprise Edition, or Windows Server 2003, Datacenter Edition.

## -see-also

<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset">IVssBackupComponents::DoSnapshotSet</a>



<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-exposesnapshot">IVssBackupComponents::ExposeSnapshot</a>



<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-setcontext">IVssBackupComponents::SetContext</a>



<a href="/windows/desktop/api/vss/ns-vss-vss_object_prop">VSS_OBJECT_PROP</a>



<a href="/windows/desktop/api/vss/ns-vss-vss_snapshot_prop">VSS_SNAPSHOT_PROP</a>



<a href="/windows/desktop/api/vss/ne-vss-vss_volume_snapshot_attributes">_VSS_VOLUME_SNAPSHOT_ATTRIBUTES</a>
