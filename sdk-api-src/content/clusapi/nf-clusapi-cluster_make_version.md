---
UID: NF:clusapi.CLUSTER_MAKE_VERSION
title: CLUSTER_MAKE_VERSION macro (clusapi.h)
author: windows-sdk-content
description: Creates a Cluster service version number.
old-location: mscs\cluster_make_version.htm
tech.root: MsCS
ms.assetid: 0a53c070-efed-4105-8dce-60647869a93f
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CLUSTER_MAKE_VERSION, CLUSTER_MAKE_VERSION macro [Failover Cluster], _wolf_cluster_make_version, clusapi/CLUSTER_MAKE_VERSION, mscs.cluster_make_version
ms.topic: macro
f1_keywords: 
 - "clusapi/CLUSTER_MAKE_VERSION"
dev_langs:
 - c++
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ClusAPI.h
api_name:
 - CLUSTER_MAKE_VERSION
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# CLUSTER_MAKE_VERSION macro


## -description


Creates a Cluster service version number.


## -parameters




### -param _maj

Major version number.


### -param _min

Minor version number.


## -remarks



Cluster service version numbers are obtained from the  <a href="https://docs.microsoft.com/previous-versions/windows/desktop/mscs/nodes-nodehighestversion">NodeHighestVersion</a> and  <a href="https://docs.microsoft.com/previous-versions/windows/desktop/mscs/nodes-nodelowestversion">NodeLowestVersion</a> properties as well as the function  <a href="https://docs.microsoft.com/windows/desktop/api/clusapi/nf-clusapi-getclusterinformation">GetClusterInformation</a>. For more information, see  <a href="https://docs.microsoft.com/previous-versions/windows/desktop/mscs/version-compatibility">Version Compatibility</a>.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/clusapi/nf-clusapi-cluster_get_major_version">CLUSTER_GET_MAJOR_VERSION</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/clusapi/nf-clusapi-cluster_get_minor_version">CLUSTER_GET_MINOR_VERSION</a>
 

 

