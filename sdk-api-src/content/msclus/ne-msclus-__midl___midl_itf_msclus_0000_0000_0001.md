---
UID: NE:msclus.__MIDL___MIDL_itf_msclus_0000_0000_0001
title: "__MIDL___MIDL_itf_msclus_0000_0000_0001"
author: windows-sdk-content
description: Specifies the type of cluster group to create.
old-location: mscs\clusgroup_type.htm
tech.root: mscs
ms.assetid: E3937C18-A0B6-44ED-AA75-69940ACCBFAA
ms.author: windowssdkdev
ms.date: 11/06/2018
ms.keywords: "*PCLUSGROUP_TYPE, CLUSGROUP_TYPE, CLUSGROUP_TYPE enumeration [Failover Cluster], ClusGroupTypeAvailableStorage, ClusGroupTypeClusterUpdateAgent, ClusGroupTypeCoreCluster, ClusGroupTypeCrossClusterOrchestrator, ClusGroupTypeDhcpServer, ClusGroupTypeDtc, ClusGroupTypeFileServer, ClusGroupTypeGenericApplication, ClusGroupTypeGenericScript, ClusGroupTypeGenericService, ClusGroupTypeIScsiNameService, ClusGroupTypeIScsiTarget, ClusGroupTypeMsmq, ClusGroupTypePrintServer, ClusGroupTypeScaleoutCluster, ClusGroupTypeScaleoutFileServer, ClusGroupTypeSharedVolume, ClusGroupTypeStandAloneDfs, ClusGroupTypeStoragePool, ClusGroupTypeStorageReplica, ClusGroupTypeTaskScheduler, ClusGroupTypeTemporary, ClusGroupTypeTsSessionBroker, ClusGroupTypeUnknown, ClusGroupTypeVMReplicaBroker, ClusGroupTypeVMReplicaCoordinator, ClusGroupTypeVirtualMachine, ClusGroupTypeWins, PCLUSGROUP_TYPE, PCLUSGROUP_TYPE enumeration pointer [Failover Cluster], __MIDL___MIDL_itf_msclus_0000_0000_0001, clusapi/CLUSGROUP_TYPE, clusapi/ClusGroupTypeAvailableStorage, clusapi/ClusGroupTypeClusterUpdateAgent, clusapi/ClusGroupTypeCoreCluster, clusapi/ClusGroupTypeCrossClusterOrchestrator, clusapi/ClusGroupTypeDhcpServer, clusapi/ClusGroupTypeDtc, clusapi/ClusGroupTypeFileServer, clusapi/ClusGroupTypeGenericApplication, clusapi/ClusGroupTypeGenericScript, clusapi/ClusGroupTypeGenericService, clusapi/ClusGroupTypeIScsiNameService, clusapi/ClusGroupTypeIScsiTarget, clusapi/ClusGroupTypeMsmq, clusapi/ClusGroupTypePrintServer, clusapi/ClusGroupTypeScaleoutCluster, clusapi/ClusGroupTypeScaleoutFileServer, clusapi/ClusGroupTypeSharedVolume, clusapi/ClusGroupTypeStandAloneDfs, clusapi/ClusGroupTypeStoragePool, clusapi/ClusGroupTypeStorageReplica, clusapi/ClusGroupTypeTaskScheduler, clusapi/ClusGroupTypeTemporary, clusapi/ClusGroupTypeTsSessionBroker, clusapi/ClusGroupTypeUnknown, clusapi/ClusGroupTypeVMReplicaBroker, clusapi/ClusGroupTypeVMReplicaCoordinator, clusapi/ClusGroupTypeVirtualMachine, clusapi/ClusGroupTypeWins, clusapi/PCLUSGROUP_TYPE, msclus/CLUSGROUP_TYPE, msclus/ClusGroupTypeAvailableStorage, msclus/ClusGroupTypeClusterUpdateAgent, msclus/ClusGroupTypeCoreCluster, msclus/ClusGroupTypeCrossClusterOrchestrator, msclus/ClusGroupTypeDhcpServer, msclus/ClusGroupTypeDtc, msclus/ClusGroupTypeFileServer, msclus/ClusGroupTypeGenericApplication, msclus/ClusGroupTypeGenericScript, msclus/ClusGroupTypeGenericService, msclus/ClusGroupTypeIScsiNameService, msclus/ClusGroupTypeIScsiTarget, msclus/ClusGroupTypeMsmq, msclus/ClusGroupTypePrintServer, msclus/ClusGroupTypeScaleoutCluster, msclus/ClusGroupTypeScaleoutFileServer, msclus/ClusGroupTypeSharedVolume, msclus/ClusGroupTypeStandAloneDfs, msclus/ClusGroupTypeStoragePool, msclus/ClusGroupTypeStorageReplica, msclus/ClusGroupTypeTaskScheduler, msclus/ClusGroupTypeTemporary, msclus/ClusGroupTypeTsSessionBroker, msclus/ClusGroupTypeUnknown, msclus/ClusGroupTypeVMReplicaBroker, msclus/ClusGroupTypeVMReplicaCoordinator, msclus/ClusGroupTypeVirtualMachine, msclus/ClusGroupTypeWins, msclus/PCLUSGROUP_TYPE, mscs.clusgroup_type"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: msclus.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2012
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ClusApi.h
 - MsClus.h
api_name:
 - CLUSGROUP_TYPE
product: Windows
targetos: Windows
req.typenames: CLUSGROUP_TYPE, *PCLUSGROUP_TYPE
req.redist: 
---

# __MIDL___MIDL_itf_msclus_0000_0000_0001 enumeration


## -description


Specifies the type of cluster group to create.


## -enum-fields




### -field ClusGroupTypeCoreCluster

A core cluster group.


### -field ClusGroupTypeAvailableStorage

An available storage cluster group.


### -field ClusGroupTypeTemporary

A temporary cluster group.


### -field ClusGroupTypeSharedVolume

A shared volume.


### -field ClusGroupTypeStoragePool

A storage pool.


### -field ClusGroupTypeFileServer

A file server.


### -field ClusGroupTypePrintServer

A print server.


### -field ClusGroupTypeDhcpServer

A Dynamic Host Configuration Protocol (DHCP) server.


### -field ClusGroupTypeDtc

A Distributed Transaction Coordinator (DTC) service.


### -field ClusGroupTypeMsmq

An Microsoft Message Queuing (MSMQ) service.


### -field ClusGroupTypeWins

A Windows Internet Name Service (WINS).


### -field ClusGroupTypeStandAloneDfs

A standalone Distributed File System (DFS).


### -field ClusGroupTypeGenericApplication

A generic application.


### -field ClusGroupTypeGenericService

A generic service.


### -field ClusGroupTypeGenericScript

A generic script.


### -field ClusGroupTypeIScsiNameService

An  Internet Small Computer System Interface (iSCSI) name service.


### -field ClusGroupTypeVirtualMachine

A virtual machine.


### -field ClusGroupTypeTsSessionBroker

A Terminal Services  Session  Broker.


### -field ClusGroupTypeIScsiTarget

An iSCSI target.


### -field ClusGroupTypeScaleoutFileServer

A Scale-Out File Server.


### -field ClusGroupTypeVMReplicaBroker

A virtual machine  replica broker.


### -field ClusGroupTypeTaskScheduler

A task scheduler.


### -field ClusGroupTypeClusterUpdateAgent

A cluster update agent.


### -field ClusGroupTypeScaleoutCluster

A cluster on a scale-out file server.

<b>Windows Server 2012 R2 and Windows Server 2012:  </b>This member is not supported until Windows Server 2016.


### -field ClusGroupTypeStorageReplica

A storage replica.

<b>Windows Server 2012 R2 and Windows Server 2012:  </b>This member is not supported until Windows Server 2016.


### -field ClusGroupTypeVMReplicaCoordinator

A virtual machine replica coordinator.

<b>Windows Server 2012 R2 and Windows Server 2012:  </b>This member is not supported until Windows Server 2016.


### -field ClusGroupTypeCrossClusterOrchestrator

A cross-cluster orchestrator.

<b>Windows Server 2012 R2 and Windows Server 2012:  </b>This member is not supported until Windows Server 2016.


### -field ClusGroupTypeInfrastructureFileServer


### -field ClusGroupTypeUnknown

An unknown cluster group type.


## -see-also




<a href="https://msdn.microsoft.com/546071de-1067-4b47-b862-668be976e563">Failover Cluster Enumerations</a>
 

 

