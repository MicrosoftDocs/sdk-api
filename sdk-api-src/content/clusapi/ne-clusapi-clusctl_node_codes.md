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

# CLUSCTL_NODE_CODES enumeration


## -description


Enumerates <a href="https://msdn.microsoft.com/4381e378-7bf2-4dbc-b56e-3fed33193d32">node</a>
<a href="https://msdn.microsoft.com/b8ab57bd-f83e-46c2-9c9c-02107c3881bf">control codes</a>.


## -enum-fields




### -field CLUSCTL_NODE_UNKNOWN

See <a href="https://msdn.microsoft.com/c52faae4-aadc-4415-8858-d578273a1ecb">CLUSCTL_NODE_UNKNOWN</a>.


### -field CLUSCTL_NODE_GET_CHARACTERISTICS

See 
       <a href="https://msdn.microsoft.com/8979b006-5494-4587-9675-983ee9021273">CLUSCTL_NODE_GET_CHARACTERISTICS</a>.


### -field CLUSCTL_NODE_GET_FLAGS

See <a href="https://msdn.microsoft.com/f86835e1-2721-46ab-bd85-599e91d1d5bd">CLUSCTL_NODE_GET_FLAGS</a>.


### -field CLUSCTL_NODE_GET_NAME

See <a href="https://msdn.microsoft.com/9ad0c5ec-294a-4236-b179-77cafbaa95f2">CLUSCTL_NODE_GET_NAME</a>.


### -field CLUSCTL_NODE_GET_ID

See <a href="https://msdn.microsoft.com/0222665c-f029-40d9-b568-b27ad6e78dfc">CLUSCTL_NODE_GET_ID</a>.


### -field CLUSCTL_NODE_ENUM_COMMON_PROPERTIES

See 
       <a href="https://msdn.microsoft.com/57b755e2-6f0d-4b06-aca4-6ce57627d8a3">CLUSCTL_NODE_ENUM_COMMON_PROPERTIES</a>.


### -field CLUSCTL_NODE_GET_RO_COMMON_PROPERTIES

See 
       <a href="https://msdn.microsoft.com/e7466dff-e20e-442e-a91c-b07c34d172d8">CLUSCTL_NODE_GET_RO_COMMON_PROPERTIES</a>.


### -field CLUSCTL_NODE_GET_COMMON_PROPERTIES

See 
       <a href="https://msdn.microsoft.com/5eec9b3b-7f6f-4e28-a0b1-1d5d7db2a9af">CLUSCTL_NODE_GET_COMMON_PROPERTIES</a>.


### -field CLUSCTL_NODE_SET_COMMON_PROPERTIES

See 
       <a href="https://msdn.microsoft.com/753ed089-b5ad-42b4-a947-2504c624f290">CLUSCTL_NODE_SET_COMMON_PROPERTIES</a>.


### -field CLUSCTL_NODE_VALIDATE_COMMON_PROPERTIES

See 
       <a href="https://msdn.microsoft.com/edf5e39f-3b56-47c0-b25a-934b0968ccd3">CLUSCTL_NODE_VALIDATE_COMMON_PROPERTIES</a>.


### -field CLUSCTL_NODE_ENUM_PRIVATE_PROPERTIES

See 
       <a href="https://msdn.microsoft.com/d97ffdfb-50a4-4313-9991-f9223e8bb693">CLUSCTL_NODE_ENUM_PRIVATE_PROPERTIES</a>.


### -field CLUSCTL_NODE_GET_RO_PRIVATE_PROPERTIES

See 
       <a href="https://msdn.microsoft.com/170509ac-6373-40a4-8370-835bf5d647df">CLUSCTL_NODE_GET_RO_PRIVATE_PROPERTIES</a>.


### -field CLUSCTL_NODE_GET_PRIVATE_PROPERTIES

See 
       <a href="https://msdn.microsoft.com/b22f281d-d88d-41bb-ab49-e7168e6e9f95">CLUSCTL_NODE_GET_PRIVATE_PROPERTIES</a>.


### -field CLUSCTL_NODE_SET_PRIVATE_PROPERTIES

See 
       <a href="https://msdn.microsoft.com/586b34b5-8da0-4030-922b-95afd3b1204f">CLUSCTL_NODE_SET_PRIVATE_PROPERTIES</a>.


### -field CLUSCTL_NODE_VALIDATE_PRIVATE_PROPERTIES

See 
       <a href="https://msdn.microsoft.com/9e8ebb06-53a5-45cb-b611-dda4c5d01321">CLUSCTL_NODE_VALIDATE_PRIVATE_PROPERTIES</a>.


### -field CLUSCTL_NODE_GET_COMMON_PROPERTY_FMTS

See 
       <a href="https://msdn.microsoft.com/a845a925-9725-40e7-b4d7-10cd1a5b5066">CLUSCTL_NODE_GET_COMMON_PROPERTY_FMTS</a>.


### -field CLUSCTL_NODE_GET_PRIVATE_PROPERTY_FMTS

See 
       <a href="https://msdn.microsoft.com/f66f3966-8364-42be-b59e-b6b9a034c362">CLUSCTL_NODE_GET_PRIVATE_PROPERTY_FMTS</a>.


### -field CLUSCTL_NODE_GET_CLUSTER_SERVICE_ACCOUNT_NAME

See 
       <a href="https://msdn.microsoft.com/e4210af5-d11f-4c23-abdd-746d4b662cdb">CLUSCTL_NODE_GET_CLUSTER_SERVICE_ACCOUNT_NAME</a>.


### -field CLUSCTL_NODE_GET_STUCK_NODES


### -field CLUSCTL_NODE_INJECT_GEM_FAULT

See <a href="https://msdn.microsoft.com/3E6CA343-801F-4175-98BC-1406E0A1118A">CLUSCTL_NODE_INJECT_GEM_FAULT</a>.

<b>Windows Server 2008 R2 and Windows Server 2012:  </b>This control code is not supported before Windows Server 2012 R2.




### -field CLUSCTL_NODE_INTRODUCE_GEM_REPAIR_DELAY

See <a href="https://msdn.microsoft.com/F202CC42-5E49-4BA2-8A00-A5AB24E66F62">CLUSCTL_NODE_INTRODUCE_GEM_REPAIR_DELAY</a>.

<b>Windows Server 2008 R2 and Windows Server 2012:  </b>This control code is not supported before Windows Server 2012 R2.




### -field CLUSCTL_NODE_SEND_DUMMY_GEM_MESSAGES

See <a href="https://msdn.microsoft.com/F29E4B65-01C4-4675-A429-9CAA0A1EE731">CLUSCTL_NODE_SEND_DUMMY_GEM_MESSAGES</a>.

<b>Windows Server 2008 R2 and Windows Server 2012:  </b>This control code is not supported before Windows Server 2012 R2.




### -field CLUSCTL_NODE_BLOCK_GEM_SEND_RECV

See <a href="https://msdn.microsoft.com/76DA3FA5-7529-4285-BF74-C92928ECE678">CLUSCTL_NODE_BLOCK_GEM_SEND_RECV</a>.

<b>Windows Server 2008 R2 and Windows Server 2012:  </b>This control code is not supported before Windows Server 2012 R2.




### -field CLUSCTL_NODE_GET_GEMID_VECTOR

See <a href="https://msdn.microsoft.com/29C75041-F780-46F1-958C-16496E39B031">CLUSCTL_NODE_GET_GEMID_VECTOR</a>.

<b>Windows Server 2008 R2 and Windows Server 2012:  </b>This control code is not supported before Windows Server 2012 R2.




## -see-also




<a href="https://msdn.microsoft.com/546071de-1067-4b47-b862-668be976e563">Failover Cluster Enumerations</a>



<a href="https://msdn.microsoft.com/39b59726-e00e-4011-a7bc-96698e12f1e4">Node Control Codes</a>
 

 

