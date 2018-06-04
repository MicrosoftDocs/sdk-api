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
 

 

