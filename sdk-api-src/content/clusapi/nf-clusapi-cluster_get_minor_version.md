---
UID: NF:clusapi.CLUSTER_GET_MINOR_VERSION
title: CLUSTER_GET_MINOR_VERSION macro (clusapi.h)
description: Extracts the minor version portion of a Cluster service version number.
helpviewer_keywords: ["CLUSTER_GET_MINOR_VERSION","CLUSTER_GET_MINOR_VERSION macro [Failover Cluster]","_wolf_cluster_get_minor_version","clusapi/CLUSTER_GET_MINOR_VERSION","mscs.cluster_get_minor_version"]
old-location: mscs\cluster_get_minor_version.htm
tech.root: MsCS
ms.assetid: 90caa255-9b04-4b83-a846-78590bfce3a7
ms.date: 12/05/2018
ms.keywords: CLUSTER_GET_MINOR_VERSION, CLUSTER_GET_MINOR_VERSION macro [Failover Cluster], _wolf_cluster_get_minor_version, clusapi/CLUSTER_GET_MINOR_VERSION, mscs.cluster_get_minor_version
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CLUSTER_GET_MINOR_VERSION
 - clusapi/CLUSTER_GET_MINOR_VERSION
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
 - CLUSTER_GET_MINOR_VERSION
---

# CLUSTER_GET_MINOR_VERSION macro


## -description

Extracts the minor version portion of a  <a href="/previous-versions/windows/desktop/mscs/cluster-service">Cluster service</a> version number.

## -parameters

### -param _ver

Cluster service version number.

## -remarks

Cluster service version numbers are obtained from the  <a href="/previous-versions/windows/desktop/mscs/nodes-nodehighestversion">NodeHighestVersion</a> and  <a href="/previous-versions/windows/desktop/mscs/nodes-nodelowestversion">NodeLowestVersion</a> properties as well as the function  <a href="/windows/desktop/api/clusapi/nf-clusapi-getclusterinformation">GetClusterInformation</a>. For more information, see  <a href="/previous-versions/windows/desktop/mscs/version-compatibility">Version Compatibility</a>.

In Windows Server 2016 Minor version has been renamed to upgrade version, but the <b>CLUSTER_GET_MINOR_VERSION</b> macro remains for compatibility.

## -see-also

<a href="/previous-versions/windows/desktop/api/clusapi/nf-clusapi-cluster_get_major_version">CLUSTER_GET_MAJOR_VERSION</a>



<a href="/previous-versions/windows/desktop/api/clusapi/nf-clusapi-cluster_get_upgrade_version">CLUSTER_GET_UPGRADE_VERSION</a>



<a href="/previous-versions/windows/desktop/api/clusapi/nf-clusapi-cluster_make_version">CLUSTER_MAKE_VERSION</a>