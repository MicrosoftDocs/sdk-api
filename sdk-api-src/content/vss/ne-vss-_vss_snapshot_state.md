---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# _VSS_SNAPSHOT_STATE enumeration


## -description


The <b>VSS_SNAPSHOT_STATE</b> enumeration is returned by a 
    provider to specify the state of a given shadow copy operation.


## -enum-fields




### -field VSS_SS_UNKNOWN

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
    <a href="https://msdn.microsoft.com/070ec204-e751-4ebf-8f99-3c415f203cb2">VSS_SNAPSHOT_PROP</a> object, which can be obtained for a 
    single shadow copy by calling 
    <a href="https://msdn.microsoft.com/a4e2f9f3-7dee-4324-a48a-6de2a32eabf7">IVssBackupComponents::GetSnapshotProperties</a>.

Because 
    <a href="https://msdn.microsoft.com/a4e2f9f3-7dee-4324-a48a-6de2a32eabf7">IVssBackupComponents::GetSnapshotProperties</a> 
    fails during shadow copy creation with <b>VSS_E_OBJECT_NOT_FOUND</b>, a requester cannot obtain 
    any <b>VSS_SNAPSHOT_STATE</b> value other than 
    <b>VSS_SS_CREATED</b>.

Calls to <a href="https://msdn.microsoft.com/3f79bf84-c7b9-4291-ae3b-7061fe3199e9">IVssBackupComponents::Query</a> can 
    also be used to obtain the shadow copy state. 
    <b>IVssBackupComponents::Query</b> is used to return 
    lists of shadow copies, which may be iterated over by means of the 
    <a href="https://msdn.microsoft.com/b8e80909-a28a-45d7-87e2-4f44bf6990f4">IVssEnumObject</a> interface to obtain 
    <a href="https://msdn.microsoft.com/070ec204-e751-4ebf-8f99-3c415f203cb2">VSS_SNAPSHOT_PROP</a> objects for each shadow copy that 
    have completed on a given system. This means that, like 
    <a href="https://msdn.microsoft.com/a4e2f9f3-7dee-4324-a48a-6de2a32eabf7">IVssBackupComponents::GetSnapshotProperties</a>, 
    the <b>IVssBackupComponents::Query</b> method can 
    return only a shadow copy state of <b>VSS_SS_CREATED</b>.




## -see-also




<a href="https://msdn.microsoft.com/a4e2f9f3-7dee-4324-a48a-6de2a32eabf7">IVssBackupComponents::GetSnapshotProperties</a>



<a href="https://msdn.microsoft.com/3f79bf84-c7b9-4291-ae3b-7061fe3199e9">IVssBackupComponents::Query</a>



<a href="https://msdn.microsoft.com/b8e80909-a28a-45d7-87e2-4f44bf6990f4">IVssEnumObject</a>



<a href="https://msdn.microsoft.com/90664042-e9a0-4959-a975-9289477d2394">VSS_OBJECT_PROP</a>



<a href="https://msdn.microsoft.com/e8d70f20-00a9-4cae-a92c-e3f3673a8db3">VSS_OBJECT_UNION</a>



<a href="https://msdn.microsoft.com/070ec204-e751-4ebf-8f99-3c415f203cb2">VSS_SNAPSHOT_PROP</a>
 

 

