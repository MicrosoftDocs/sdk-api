---
UID: NS:clusapi.CLUSTERVERSIONINFO
title: CLUSTERVERSIONINFO (clusapi.h)
description: Describes information about the version of the Cluster service installed locally on a node.
helpviewer_keywords: ["*LPCLUSTERVERSIONINFO","*PCLUSTERVERSIONINFO","CLUSTERVERSIONINFO","CLUSTERVERSIONINFO structure [Failover Cluster]","LPCLUSTERVERSIONINFO","LPCLUSTERVERSIONINFO structure pointer [Failover Cluster]","PCLUSTERVERSIONINFO","PCLUSTERVERSIONINFO structure pointer [Failover Cluster]","_wolf_clusterversioninfo","clusapi/CLUSTERVERSIONINFO","clusapi/LPCLUSTERVERSIONINFO","clusapi/PCLUSTERVERSIONINFO","mscs.clusterversioninfo"]
old-location: mscs\clusterversioninfo.htm
tech.root: MsCS
ms.assetid: e1cecdbc-f0e4-4ee8-9a97-14859ceba5fd
ms.date: 12/05/2018
ms.keywords: '*LPCLUSTERVERSIONINFO, *PCLUSTERVERSIONINFO, CLUSTERVERSIONINFO, CLUSTERVERSIONINFO structure [Failover Cluster], LPCLUSTERVERSIONINFO, LPCLUSTERVERSIONINFO structure pointer [Failover Cluster], PCLUSTERVERSIONINFO, PCLUSTERVERSIONINFO structure pointer [Failover Cluster], _wolf_clusterversioninfo, clusapi/CLUSTERVERSIONINFO, clusapi/LPCLUSTERVERSIONINFO, clusapi/PCLUSTERVERSIONINFO, mscs.clusterversioninfo'
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
req.typenames: CLUSTERVERSIONINFO, *LPCLUSTERVERSIONINFO, *PCLUSTERVERSIONINFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CLUSTERVERSIONINFO
 - clusapi/CLUSTERVERSIONINFO
 - LPCLUSTERVERSIONINFO
 - clusapi/LPCLUSTERVERSIONINFO
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
 - CLUSTERVERSIONINFO
---

# CLUSTERVERSIONINFO structure


## -description

Describes 
    information about the version of the <a href="/previous-versions/windows/desktop/mscs/cluster-service">Cluster service</a> 
    installed locally on a <a href="/previous-versions/windows/desktop/mscs/nodes">node</a>.

## -struct-fields

### -field dwVersionInfoSize

Size, in bytes, of the data structure. Users must set this size prior to calling 
      <a href="/windows/desktop/api/clusapi/nf-clusapi-getclusterinformation">GetClusterInformation</a>.

### -field MajorVersion

Identifies the major version number of the operating system installed on the local node. For example, for 
      version X.Y, the major version number is X.

### -field MinorVersion

Identifies the minor version number of the operating system installed on the local node. For example, for 
      version X.Y, the minor version number is Y.

### -field BuildNumber

Identifies the build number of the operating system installed on the local node, such as 224.

### -field szVendorId

Contains the vendor identifier information for the Cluster service installed on the local node.

### -field szCSDVersion

Contains the latest service pack installed on the node. If a Service Pack has not been installed, the 
      <b>szCSDVersion</b> member is empty.

### -field dwClusterHighestVersion

Identifies the highest version of the Cluster service with which the Cluster service installed on the local 
      node can join to form a <a href="/previous-versions/windows/desktop/mscs/c-gly">cluster</a>.

### -field dwClusterLowestVersion

Identifies the lowest version of the Cluster service with which the Cluster service installed on the local 
      node can join to form a cluster.

### -field dwFlags

If the cluster nodes are running different versions of the Cluster service, this value is set to 
      <b>CLUSTER_VERSION_FLAG_MIXED_MODE</b>. If all cluster nodes are running the same version of 
      the <a href="/previous-versions/windows/desktop/mscs/cluster-service">Cluster service</a>, this value is 0.

### -field dwReserved

This value is reserved for internal use.

## -remarks

To obtain cluster version information, applications declare a 
    <b>CLUSTERVERSIONINFO</b> structure, specify the size of the 
    structure in the <b>dwVersionInfoSize</b> member, and call the 
    <a href="/windows/desktop/api/clusapi/nf-clusapi-getclusterinformation">GetClusterInformation</a> function. 
    <b>GetClusterInformation</b> fills in the structure 
    member data.

To prevent overwrites for all possible combinations of version information, always set 
    <b>dwVersionInfoSize</b> to:

<code>sizeof(CLUSTERVERSIONINFO)</code>

The <b>dwClusterHighestVersion</b> and <b>dwClusterLowestVersion</b> 
    values indicate whether the local node can join with another node to form a cluster. A join can succeed if one of 
    the following is true:

<ul>
<li>The local node's highest version exactly matches the other node's highest version.</li>
<li>The local node's lowest version exactly matches the other node's highest version.</li>
<li>The local node's highest version exactly matches the other node's lowest version.</li>
</ul>
For more information on how the Cluster service creates and uses version numbers, see 
    <a href="/previous-versions/windows/desktop/mscs/version-compatibility">Version Compatibility</a>.

## -see-also

<a href="/windows/desktop/api/clusapi/nf-clusapi-getclusterinformation">GetClusterInformation</a>