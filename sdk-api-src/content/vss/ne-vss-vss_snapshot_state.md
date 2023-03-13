---
UID: NE:vss._VSS_SNAPSHOT_STATE
title: VSS_SNAPSHOT_STATE (vss.h)
description: Specify the state of a given shadow copy operation.
helpviewer_keywords: ["*PVSS_SNAPSHOT_STATE","PVSS_SNAPSHOT_STATE","PVSS_SNAPSHOT_STATE enumeration pointer [VSS]","VSS_SNAPSHOT_STATE","VSS_SNAPSHOT_STATE enumeration [VSS]","VSS_SS_ABORTED","VSS_SS_COMMITTED","VSS_SS_COUNT","VSS_SS_CREATED","VSS_SS_DELETED","VSS_SS_POSTCOMMITTED","VSS_SS_PRECOMMITTED","VSS_SS_PREFINALCOMMITTED","VSS_SS_PREPARED","VSS_SS_PREPARING","VSS_SS_PROCESSING_COMMIT","VSS_SS_PROCESSING_POSTCOMMIT","VSS_SS_PROCESSING_POSTFINALCOMMIT","VSS_SS_PROCESSING_PRECOMMIT","VSS_SS_PROCESSING_PREFINALCOMMIT","VSS_SS_PROCESSING_PREPARE","VSS_SS_UNKNOWN","_win32_vss_snapshot_state","base.vss_snapshot_state","vss/PVSS_SNAPSHOT_STATE","vss/VSS_SNAPSHOT_STATE","vss/VSS_SS_ABORTED","vss/VSS_SS_COMMITTED","vss/VSS_SS_COUNT","vss/VSS_SS_CREATED","vss/VSS_SS_DELETED","vss/VSS_SS_POSTCOMMITTED","vss/VSS_SS_PRECOMMITTED","vss/VSS_SS_PREFINALCOMMITTED","vss/VSS_SS_PREPARED","vss/VSS_SS_PREPARING","vss/VSS_SS_PROCESSING_COMMIT","vss/VSS_SS_PROCESSING_POSTCOMMIT","vss/VSS_SS_PROCESSING_POSTFINALCOMMIT","vss/VSS_SS_PROCESSING_PRECOMMIT","vss/VSS_SS_PROCESSING_PREFINALCOMMIT","vss/VSS_SS_PROCESSING_PREPARE","vss/VSS_SS_UNKNOWN"]
old-location: base\vss_snapshot_state.htm
tech.root: base
ms.assetid: 0f9ce651-c9ad-454f-88a5-1f877c7c06ca
ms.date: 12/05/2018
ms.keywords: '*PVSS_SNAPSHOT_STATE, PVSS_SNAPSHOT_STATE, PVSS_SNAPSHOT_STATE enumeration pointer [VSS], VSS_SNAPSHOT_STATE, VSS_SNAPSHOT_STATE enumeration [VSS], VSS_SS_ABORTED, VSS_SS_COMMITTED, VSS_SS_COUNT, VSS_SS_CREATED, VSS_SS_DELETED, VSS_SS_POSTCOMMITTED, VSS_SS_PRECOMMITTED, VSS_SS_PREFINALCOMMITTED, VSS_SS_PREPARED, VSS_SS_PREPARING, VSS_SS_PROCESSING_COMMIT, VSS_SS_PROCESSING_POSTCOMMIT, VSS_SS_PROCESSING_POSTFINALCOMMIT, VSS_SS_PROCESSING_PRECOMMIT, VSS_SS_PROCESSING_PREFINALCOMMIT, VSS_SS_PROCESSING_PREPARE, VSS_SS_UNKNOWN, _win32_vss_snapshot_state, base.vss_snapshot_state, vss/PVSS_SNAPSHOT_STATE, vss/VSS_SNAPSHOT_STATE, vss/VSS_SS_ABORTED, vss/VSS_SS_COMMITTED, vss/VSS_SS_COUNT, vss/VSS_SS_CREATED, vss/VSS_SS_DELETED, vss/VSS_SS_POSTCOMMITTED, vss/VSS_SS_PRECOMMITTED, vss/VSS_SS_PREFINALCOMMITTED, vss/VSS_SS_PREPARED, vss/VSS_SS_PREPARING, vss/VSS_SS_PROCESSING_COMMIT, vss/VSS_SS_PROCESSING_POSTCOMMIT, vss/VSS_SS_PROCESSING_POSTFINALCOMMIT, vss/VSS_SS_PROCESSING_PRECOMMIT, vss/VSS_SS_PROCESSING_PREFINALCOMMIT, vss/VSS_SS_PROCESSING_PREPARE, vss/VSS_SS_UNKNOWN'
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
req.typenames: VSS_SNAPSHOT_STATE, *PVSS_SNAPSHOT_STATE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _VSS_SNAPSHOT_STATE
 - vss/_VSS_SNAPSHOT_STATE
 - PVSS_SNAPSHOT_STATE
 - vss/PVSS_SNAPSHOT_STATE
 - VSS_SNAPSHOT_STATE
 - vss/VSS_SNAPSHOT_STATE
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
 - VSS_SNAPSHOT_STATE
---

# VSS_SNAPSHOT_STATE enumeration


## -description

The <b>VSS_SNAPSHOT_STATE</b> enumeration is returned by a 
    provider to specify the state of a given shadow copy operation.

## -enum-fields

### -field VSS_SS_UNKNOWN:0

Reserved for system use. 
      

Unknown shadow copy state.

### -field VSS_SS_PREPARING

Reserved for system use. 
      

Shadow copy is being prepared.

### -field VSS_SS_PROCESSING_PREPARE

Reserved for system use. 
      

Processing of the shadow copy preparation is in progress.

### -field VSS_SS_PREPARED

Reserved for system use. 
      

Shadow copy has been prepared.

### -field VSS_SS_PROCESSING_PRECOMMIT

Reserved for system use. 
      

Processing of the shadow copy precommit is in process.

### -field VSS_SS_PRECOMMITTED

Reserved for system use. 
      

Shadow copy is precommitted.

### -field VSS_SS_PROCESSING_COMMIT

Reserved for system use. 
      

Processing of the shadow copy commit is in process.

### -field VSS_SS_COMMITTED

Reserved for system use. 
      

Shadow copy is committed.

### -field VSS_SS_PROCESSING_POSTCOMMIT

Reserved for system use. 
      

Processing of the shadow copy postcommit is in process.

### -field VSS_SS_PROCESSING_PREFINALCOMMIT

Reserved for system use.
      

Processing of the shadow copy file commit operation is underway.

### -field VSS_SS_PREFINALCOMMITTED

Reserved for system use. 
      

Processing of the shadow copy file commit operation is done.

### -field VSS_SS_PROCESSING_POSTFINALCOMMIT

Reserved for system use.
      

Processing of the shadow copy following the final commit and prior to shadow copy create is underway.

### -field VSS_SS_CREATED

Shadow copy is created.

### -field VSS_SS_ABORTED

Reserved for system use. 
      

Shadow copy creation is aborted.

### -field VSS_SS_DELETED

Reserved for system use. 
      

Shadow copy has been deleted.

### -field VSS_SS_POSTCOMMITTED

### -field VSS_SS_COUNT

Reserved value.

## -remarks

The shadow copy state is contained in the <b>m_eStatus</b> member of a 
    <a href="/windows/desktop/api/vss/ns-vss-vss_snapshot_prop">VSS_SNAPSHOT_PROP</a> object, which can be obtained for a 
    single shadow copy by calling 
    <a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-getsnapshotproperties">IVssBackupComponents::GetSnapshotProperties</a>.

Because 
    <a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-getsnapshotproperties">IVssBackupComponents::GetSnapshotProperties</a> 
    fails during shadow copy creation with <b>VSS_E_OBJECT_NOT_FOUND</b>, a requester cannot obtain 
    any <b>VSS_SNAPSHOT_STATE</b> value other than 
    <b>VSS_SS_CREATED</b>.

Calls to <a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-query">IVssBackupComponents::Query</a> can 
    also be used to obtain the shadow copy state. 
    <b>IVssBackupComponents::Query</b> is used to return 
    lists of shadow copies, which may be iterated over by means of the 
    <a href="/windows/desktop/api/vss/nn-vss-ivssenumobject">IVssEnumObject</a> interface to obtain 
    <a href="/windows/desktop/api/vss/ns-vss-vss_snapshot_prop">VSS_SNAPSHOT_PROP</a> objects for each shadow copy that 
    have completed on a given system. This means that, like 
    <a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-getsnapshotproperties">IVssBackupComponents::GetSnapshotProperties</a>, 
    the <b>IVssBackupComponents::Query</b> method can 
    return only a shadow copy state of <b>VSS_SS_CREATED</b>.

## -see-also

<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-getsnapshotproperties">IVssBackupComponents::GetSnapshotProperties</a>



<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-query">IVssBackupComponents::Query</a>



<a href="/windows/desktop/api/vss/nn-vss-ivssenumobject">IVssEnumObject</a>



<a href="/windows/desktop/api/vss/ns-vss-vss_object_prop">VSS_OBJECT_PROP</a>



<a href="/windows/desktop/api/vss/ns-vss-vss_snapshot_prop">VSS_SNAPSHOT_PROP</a>

