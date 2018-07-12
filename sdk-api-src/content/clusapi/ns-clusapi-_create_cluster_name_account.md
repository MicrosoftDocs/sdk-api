---
UID: NS:clusapi._CREATE_CLUSTER_NAME_ACCOUNT
title: "_CREATE_CLUSTER_NAME_ACCOUNT"
author: windows-sdk-content
description: Describes a cluster name resource and domain credentials used by the CreateClusterNameAccount function to add a cluster to a domain. PCREATE_CLUSTER_NAME_ACCOUNT defines a pointer to this structure.
old-location: mscs\create_cluster_name_account.htm
old-project: mscs
ms.assetid: 21D43B28-0B14-4A00-BDEE-B2B769BF9777
ms.author: windowssdkdev
ms.date: 06/08/2018
ms.keywords: "*PCREATE_CLUSTER_NAME_ACCOUNT, CREATE_CLUSTER_NAME_ACCOUNT, CREATE_CLUSTER_NAME_ACCOUNT structure [Failover Cluster], PCREATE_CLUSTER_NAME_ACCOUNT, PCREATE_CLUSTER_NAME_ACCOUNT structure pointer [Failover Cluster], _CREATE_CLUSTER_NAME_ACCOUNT, clusapi/CREATE_CLUSTER_NAME_ACCOUNT, clusapi/PCREATE_CLUSTER_NAME_ACCOUNT, mscs.create_cluster_name_account"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: clusapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2016
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: CREATE_CLUSTER_NAME_ACCOUNT, *PCREATE_CLUSTER_NAME_ACCOUNT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ClusAPI.h
api_name:
 - CREATE_CLUSTER_NAME_ACCOUNT
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _CREATE_CLUSTER_NAME_ACCOUNT structure


## -description


Describes a <a href="https://msdn.microsoft.com/7b5b9d3f-98ab-419b-936e-26e9e5fc022d">cluster name</a> resource and domain credentials used by the <a href="https://msdn.microsoft.com/82BBEE9D-C787-4935-BB5F-09438676B37A">CreateClusterNameAccount</a> function to add a cluster to a domain. <b>PCREATE_CLUSTER_NAME_ACCOUNT</b> defines a pointer to this structure.


## -struct-fields




### -field dwVersion

The major version of the OS that runs on the cluster. This member must be set to a value greater than <b>CLUSAPI_VERSION_WINDOWSBLUE</b>.


### -field lpszClusterName

The cluster name that represents the cluster on the domain.


### -field dwFlags

Reserved for future use. This value must be "0".


### -field pszUserName

The user name for the domain credentials.


### -field pszPassword

The password for the domain credentials.


### -field pszDomain

The domain name to join.


### -field managementPointType

The management point type.


### -field managementPointResType

 


### -field bUpgradeVCOs

 




## -see-also




<a href="https://msdn.microsoft.com/45da8dbc-dd70-4f95-b933-66d8e4340448">Utility Structures</a>
 

 

