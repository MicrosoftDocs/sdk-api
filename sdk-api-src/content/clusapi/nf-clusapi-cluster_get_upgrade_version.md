---
UID: NF:clusapi.CLUSTER_GET_UPGRADE_VERSION
title: CLUSTER_GET_UPGRADE_VERSION macro (clusapi.h)
description: Extracts the upgrade version portion of a Cluster service version number.
helpviewer_keywords: ["CLUSTER_GET_UPGRADE_VERSION","CLUSTER_GET_UPGRADE_VERSION macro [Failover Cluster]","clusapi/CLUSTER_GET_UPGRADE_VERSION","mscs.cluster_get_upgrade_version"]
old-location: mscs\cluster_get_upgrade_version.htm
tech.root: MsCS
ms.assetid: 28C51A05-7BCC-4394-B4D7-505750C045E2
ms.date: 12/05/2018
ms.keywords: CLUSTER_GET_UPGRADE_VERSION, CLUSTER_GET_UPGRADE_VERSION macro [Failover Cluster], clusapi/CLUSTER_GET_UPGRADE_VERSION, mscs.cluster_get_upgrade_version
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CLUSTER_GET_UPGRADE_VERSION
 - clusapi/CLUSTER_GET_UPGRADE_VERSION
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
 - CLUSTER_GET_UPGRADE_VERSION
---

# CLUSTER_GET_UPGRADE_VERSION macro


## -description

Extracts the upgrade version portion of a  <a href="/previous-versions/windows/desktop/mscs/cluster-service">Cluster service</a> version number.



Minor version has been renamed to upgrade version, but the <a href="/previous-versions/windows/desktop/api/clusapi/nf-clusapi-cluster_get_minor_version">CLUSTER_GET_MINOR_VERSION</a> macro remains for compatibility.

## -parameters

### -param _ver

Cluster service version number.

## -remarks

Cluster service version numbers are obtained from the  <a href="/previous-versions/windows/desktop/mscs/nodes-nodehighestversion">NodeHighestVersion</a> and  <a href="/previous-versions/windows/desktop/mscs/nodes-nodelowestversion">NodeLowestVersion</a> properties as well as the function  <a href="/windows/desktop/api/clusapi/nf-clusapi-getclusterinformation">GetClusterInformation</a>. For more information, see  <a href="/previous-versions/windows/desktop/mscs/version-compatibility">Version Compatibility</a>.

## -see-also

<a href="/previous-versions/windows/desktop/api/clusapi/nf-clusapi-cluster_get_major_version">CLUSTER_GET_MAJOR_VERSION</a>



<a href="/previous-versions/windows/desktop/api/clusapi/nf-clusapi-cluster_make_version">CLUSTER_MAKE_VERSION</a>