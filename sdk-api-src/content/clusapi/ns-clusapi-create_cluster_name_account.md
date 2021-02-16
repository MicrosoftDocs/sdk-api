---
UID: NS:clusapi._CREATE_CLUSTER_NAME_ACCOUNT
title: CREATE_CLUSTER_NAME_ACCOUNT (clusapi.h)
description: Describes a cluster name resource and domain credentials used by the CreateClusterNameAccount function to add a cluster to a domain. PCREATE_CLUSTER_NAME_ACCOUNT defines a pointer to this structure.
helpviewer_keywords: ["*PCREATE_CLUSTER_NAME_ACCOUNT","CREATE_CLUSTER_NAME_ACCOUNT","CREATE_CLUSTER_NAME_ACCOUNT structure [Failover Cluster]","PCREATE_CLUSTER_NAME_ACCOUNT","PCREATE_CLUSTER_NAME_ACCOUNT structure pointer [Failover Cluster]","clusapi/CREATE_CLUSTER_NAME_ACCOUNT","clusapi/PCREATE_CLUSTER_NAME_ACCOUNT","mscs.create_cluster_name_account"]
old-location: mscs\create_cluster_name_account.htm
tech.root: MsCS
ms.assetid: 21D43B28-0B14-4A00-BDEE-B2B769BF9777
ms.date: 12/05/2018
ms.keywords: '*PCREATE_CLUSTER_NAME_ACCOUNT, CREATE_CLUSTER_NAME_ACCOUNT, CREATE_CLUSTER_NAME_ACCOUNT structure [Failover Cluster], PCREATE_CLUSTER_NAME_ACCOUNT, PCREATE_CLUSTER_NAME_ACCOUNT structure pointer [Failover Cluster], clusapi/CREATE_CLUSTER_NAME_ACCOUNT, clusapi/PCREATE_CLUSTER_NAME_ACCOUNT, mscs.create_cluster_name_account'
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: CREATE_CLUSTER_NAME_ACCOUNT, *PCREATE_CLUSTER_NAME_ACCOUNT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CREATE_CLUSTER_NAME_ACCOUNT
 - clusapi/_CREATE_CLUSTER_NAME_ACCOUNT
 - PCREATE_CLUSTER_NAME_ACCOUNT
 - clusapi/PCREATE_CLUSTER_NAME_ACCOUNT
 - CREATE_CLUSTER_NAME_ACCOUNT
 - clusapi/CREATE_CLUSTER_NAME_ACCOUNT
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ClusAPI.h
api_name:
 - CREATE_CLUSTER_NAME_ACCOUNT
---

# CREATE_CLUSTER_NAME_ACCOUNT structure


## -description

Describes a <a href="/previous-versions/windows/desktop/mscs/network-name">cluster name</a> resource and domain credentials used by the <a href="/windows/desktop/api/clusapi/nf-clusapi-createclusternameaccount">CreateClusterNameAccount</a> function to add a cluster to a domain. <b>PCREATE_CLUSTER_NAME_ACCOUNT</b> defines a pointer to this structure.

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

<a href="/previous-versions/windows/desktop/mscs/utility-structures">Utility Structures</a>