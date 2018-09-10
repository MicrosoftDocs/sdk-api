---
UID: NF:clusapi.ClusterResourceControl
title: ClusterResourceControl function
author: windows-sdk-content
description: Initiates an operation affecting a resource. The operation performed depends on the control code passed to the dwControlCode parameter.
old-location: mscs\clusterresourcecontrol.htm
tech.root: mscs
ms.assetid: a98ca55a-6535-48cf-a925-5005baa01b94
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: ClusterResourceControl, ClusterResourceControl function [Failover Cluster], _wolf_clusterresourcecontrol, clusapi/ClusterResourceControl, mscs.clusterresourcecontrol
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: clusapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 Enterprise, Windows Server 2008 Datacenter
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: ClusAPI.lib
req.dll: ClusAPI.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ClusAPI.dll
 - Ext-MS-Win-Cluster-ClusAPI-l1-1-0.dll
 - Ext-MS-Win-Cluster-ClusAPI-l1-1-1.dll
 - Ext-MS-Win-Cluster-ClusAPI-l1-1-2.dll
api_name:
 - ClusterResourceControl
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ClusterResourceControl function


## -description


Initiates 
    an operation affecting a <a href="https://msdn.microsoft.com/en-us/library/Aa372152(v=VS.85).aspx">resource</a>. The operation performed 
    depends on the <a href="https://msdn.microsoft.com/en-us/library/Aa369307(v=VS.85).aspx">control code</a> passed to the 
    <i>dwControlCode</i> parameter.


## -parameters




### -param hResource [in]

Handle to the resource to be affected.


### -param hHostNode [in, optional]

Optional handle to the node to perform the operation. If <b>NULL</b>, the node that owns 
       the resource identified by <i>hResource</i> performs the operation.


### -param dwControlCode [in]

A <a href="https://msdn.microsoft.com/en-us/library/Aa372232(v=VS.85).aspx">resource control code</a>, enumerated by the 
       <a href="https://msdn.microsoft.com/en-us/library/Cc307921(v=VS.85).aspx">CLUSCTL_RESOURCE_CODES</a> enumeration, specifying 
       the operation to be performed. For the syntax associated with a control code, refer to  
       <a href="https://msdn.microsoft.com/en-us/library/Aa369308(v=VS.85).aspx">Control Code Architecture</a> and the following 
       topics:

<ul>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa367686(v=VS.85).aspx">CLUSCTL_RESOURCE_UNKNOWN</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa367466(v=VS.85).aspx">CLUSCTL_RESOURCE_GET_CHARACTERISTICS</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa367471(v=VS.85).aspx">CLUSCTL_RESOURCE_GET_FLAGS</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa367467(v=VS.85).aspx">CLUSCTL_RESOURCE_GET_CLASS_INFO</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa367479(v=VS.85).aspx">CLUSCTL_RESOURCE_GET_REQUIRED_DEPENDENCIES</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa367474(v=VS.85).aspx">CLUSCTL_RESOURCE_GET_NAME</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa367472(v=VS.85).aspx">CLUSCTL_RESOURCE_GET_ID</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa367480(v=VS.85).aspx">CLUSCTL_RESOURCE_GET_RESOURCE_TYPE</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa367461(v=VS.85).aspx">CLUSCTL_RESOURCE_ENUM_COMMON_PROPERTIES</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa367481(v=VS.85).aspx">CLUSCTL_RESOURCE_GET_RO_COMMON_PROPERTIES</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa367468(v=VS.85).aspx">CLUSCTL_RESOURCE_GET_COMMON_PROPERTIES</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa367489(v=VS.85).aspx">CLUSCTL_RESOURCE_SET_COMMON_PROPERTIES</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa367726(v=VS.85).aspx">CLUSCTL_RESOURCE_VALIDATE_COMMON_PROPERTIES</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa367469(v=VS.85).aspx">CLUSCTL_RESOURCE_GET_COMMON_PROPERTY_FMTS</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa367463(v=VS.85).aspx">CLUSCTL_RESOURCE_ENUM_PRIVATE_PROPERTIES</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa367482(v=VS.85).aspx">CLUSCTL_RESOURCE_GET_RO_PRIVATE_PROPERTIES</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa367476(v=VS.85).aspx">CLUSCTL_RESOURCE_GET_PRIVATE_PROPERTIES</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa367492(v=VS.85).aspx">CLUSCTL_RESOURCE_SET_PRIVATE_PROPERTIES</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa367728(v=VS.85).aspx">CLUSCTL_RESOURCE_VALIDATE_PRIVATE_PROPERTIES</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa367477(v=VS.85).aspx">CLUSCTL_RESOURCE_GET_PRIVATE_PROPERTY_FMTS</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa367450(v=VS.85).aspx">CLUSCTL_RESOURCE_ADD_REGISTRY_CHECKPOINT</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa367460(v=VS.85).aspx">CLUSCTL_RESOURCE_DELETE_REGISTRY_CHECKPOINT</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa367478(v=VS.85).aspx">CLUSCTL_RESOURCE_GET_REGISTRY_CHECKPOINTS</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa367443(v=VS.85).aspx">CLUSCTL_RESOURCE_ADD_CRYPTO_CHECKPOINT</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa367458(v=VS.85).aspx">CLUSCTL_RESOURCE_DELETE_CRYPTO_CHECKPOINT</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa367470(v=VS.85).aspx">CLUSCTL_RESOURCE_GET_CRYPTO_CHECKPOINTS</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa367473(v=VS.85).aspx">CLUSCTL_RESOURCE_GET_LOADBAL_PROCESS_LIST</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa367475(v=VS.85).aspx">CLUSCTL_RESOURCE_GET_NETWORK_NAME</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Bb309091(v=VS.85).aspx">CLUSCTL_RESOURCE_NETNAME_GET_VIRTUAL_SERVER_TOKEN</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Bb309093(v=VS.85).aspx">CLUSCTL_RESOURCE_NETNAME_SET_PWD_INFO</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Bb309090(v=VS.85).aspx">CLUSCTL_RESOURCE_NETNAME_DELETE_CO</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Bb309094(v=VS.85).aspx">CLUSCTL_RESOURCE_NETNAME_VALIDATE_VCO</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Cc307930(v=VS.85).aspx">CLUSCTL_RESOURCE_NETNAME_RESET_VCO</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Bb309092(v=VS.85).aspx">CLUSCTL_RESOURCE_NETNAME_REGISTER_DNS_RECORDS</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Bb309087(v=VS.85).aspx">CLUSCTL_RESOURCE_GET_DNS_NAME</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa367495(v=VS.85).aspx">CLUSCTL_RESOURCE_STORAGE_GET_DISK_INFO</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa367496(v=VS.85).aspx">CLUSCTL_RESOURCE_STORAGE_IS_PATH_VALID</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa367485(v=VS.85).aspx">CLUSCTL_RESOURCE_QUERY_DELETE</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa367688(v=VS.85).aspx">CLUSCTL_RESOURCE_UPGRADE_DLL</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Bb309089(v=VS.85).aspx">CLUSCTL_RESOURCE_IPADDRESS_RENEW_LEASE</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Bb309088(v=VS.85).aspx">CLUSCTL_RESOURCE_IPADDRESS_RELEASE_LEASE</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Bb309084(v=VS.85).aspx">CLUSCTL_RESOURCE_ADD_REGISTRY_CHECKPOINT_64BIT</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Bb309083(v=VS.85).aspx">CLUSCTL_RESOURCE_ADD_REGISTRY_CHECKPOINT_32BIT</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa367486(v=VS.85).aspx">CLUSCTL_RESOURCE_QUERY_MAINTENANCE_MODE</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa367490(v=VS.85).aspx">CLUSCTL_RESOURCE_SET_MAINTENANCE_MODE</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Bb309098(v=VS.85).aspx">CLUSCTL_RESOURCE_STORAGE_SET_DRIVELETTER</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Bb309097(v=VS.85).aspx">CLUSCTL_RESOURCE_STORAGE_GET_DISK_INFO_EX</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Cc307922(v=VS.85).aspx">CLUSCTL_RESOURCE_FILESERVER_SHARE_ADD</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Cc307923(v=VS.85).aspx">CLUSCTL_RESOURCE_FILESERVER_SHARE_DEL</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Cc307924(v=VS.85).aspx">CLUSCTL_RESOURCE_FILESERVER_SHARE_MODIFY</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Cc307925(v=VS.85).aspx">CLUSCTL_RESOURCE_FILESERVER_SHARE_REPORT</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Bb870883(v=VS.85).aspx">CLUSCTL_RESOURCE_STORAGE_GET_MOUNTPOINTS</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Cc307931(v=VS.85).aspx">CLUSCTL_RESOURCE_STORAGE_CLUSTER_DISK</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Ee342500(v=VS.85).aspx">CLUSCTL_RESOURCE_STORAGE_GET_DIRTY</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Ee342496(v=VS.85).aspx">CLUSCTL_RESOURCE_SET_CSV_MAINTENANCE_MODE</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Ee342492(v=VS.85).aspx">CLUSCTL_RESOURCE_ENABLE_SHARED_VOLUME_DIRECTIO</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Ee342491(v=VS.85).aspx">CLUSCTL_RESOURCE_DISABLE_SHARED_VOLUME_DIRECTIO</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Ee342498(v=VS.85).aspx">CLUSCTL_RESOURCE_SET_SHARED_VOLUME_BACKUP_MODE</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa367456(v=VS.85).aspx">CLUSCTL_RESOURCE_DELETE</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa367484(v=VS.85).aspx">CLUSCTL_RESOURCE_INSTALL_NODE</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa367464(v=VS.85).aspx">CLUSCTL_RESOURCE_EVICT_NODE</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa367446(v=VS.85).aspx">CLUSCTL_RESOURCE_ADD_DEPENDENCY</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa367487(v=VS.85).aspx">CLUSCTL_RESOURCE_REMOVE_DEPENDENCY</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa367448(v=VS.85).aspx">CLUSCTL_RESOURCE_ADD_OWNER</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa367488(v=VS.85).aspx">CLUSCTL_RESOURCE_REMOVE_OWNER</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa367491(v=VS.85).aspx">CLUSCTL_RESOURCE_SET_NAME</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa367452(v=VS.85).aspx">CLUSCTL_RESOURCE_CLUSTER_NAME_CHANGED</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa367453(v=VS.85).aspx">CLUSCTL_RESOURCE_CLUSTER_VERSION_CHANGED</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa367465(v=VS.85).aspx">CLUSCTL_RESOURCE_FORCE_QUORUM</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa367483(v=VS.85).aspx">CLUSCTL_RESOURCE_INITIALIZE</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa367493(v=VS.85).aspx">CLUSCTL_RESOURCE_STATE_CHANGE_REASON</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Bb309095(v=VS.85).aspx">CLUSCTL_RESOURCE_PROVIDER_STATE_CHANGE</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Cc307928(v=VS.85).aspx">CLUSCTL_RESOURCE_LEAVING_GROUP</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Cc307927(v=VS.85).aspx">CLUSCTL_RESOURCE_JOINING_GROUP</a>
</li>
<li>
<a href="https://msdn.microsoft.com/50715f64-adf2-43b5-9bd4-b5dedefa4ae8">CLUSCTL_RESOURCE_FSWITNESS_GET_EPOCH_INFO</a>
</li>
<li>
<a href="https://msdn.microsoft.com/8c46df0e-d5b6-4d69-a605-96387904a9f1">CLUSCTL_RESOURCE_FSWITNESS_SET_EPOCH_INFO</a>
</li>
<li>
<a href="https://msdn.microsoft.com/8a892ca9-fba8-4d9c-8941-bd60ceddde39">CLUSCTL_RESOURCE_FSWITNESS_RELEASE_LOCK</a>
</li>
<li>
<a href="https://msdn.microsoft.com/0965ad65-9942-4672-8ecc-c8b8fe854a85">CLUSCTL_RESOURCE_NETNAME_CREDS_UPDATED</a>
</li>
</ul>

### -param lpInBuffer [in, optional]

Pointer to an input buffer containing information needed for the operation, or <b>NULL</b> 
       if no information is needed.


### -param cbInBufferSize [in]

The allocated size (in bytes) of the input buffer.


### -param lpOutBuffer [out, optional]

Pointer to an output buffer to receive the data resulting from the operation, or 
       <b>NULL</b> if no data will be returned.


### -param cbOutBufferSize [in]

The allocated size (in bytes) of the output buffer.


### -param lpBytesReturned [out, optional]

Returns the actual size (in bytes) of the data resulting from the operation. If this information is not 
       needed, pass <b>NULL</b> for <i>lpBytesReturned</i>.


## -returns



The function returns one of the following values.




## -remarks



When <b>ClusterResourceControl</b> returns 
     <b>ERROR_MORE_DATA</b>, set <i>cbOutBufferSize</i> to the number of bytes 
     pointed to by <i>lpBytesReturned</i>, and call the function again.

Do not pass LPC and RPC handles to the same function call. Otherwise, the call will raise an RPC exception and 
     can have additional destructive effects. For information on how LPC and RPC handles are created, see 
     <a href="https://msdn.microsoft.com/0fdb2024-9b04-4a38-baf9-3cdabba9bf8c">LPC and RPC Handles</a> and 
     <a href="https://msdn.microsoft.com/b2ee2575-cc1e-4696-8e95-9798fb556c58">OpenCluster</a>.

The <b>ClusterResourceControl</b> function is one 
     of the <a href="https://msdn.microsoft.com/89ae667e-6ad9-453e-b370-b3d6a67172a2">control code functions</a>. For more information 
     on control codes and control code functions, see 
     <a href="https://msdn.microsoft.com/en-us/library/Aa372956(v=VS.85).aspx">Using Control Codes</a>.




## -see-also




<a href="https://msdn.microsoft.com/b2ee2575-cc1e-4696-8e95-9798fb556c58">OpenCluster</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa372232(v=VS.85).aspx">Resource Control Codes</a>
 

 

