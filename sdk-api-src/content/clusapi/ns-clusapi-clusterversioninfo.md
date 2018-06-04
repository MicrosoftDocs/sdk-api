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

# CLUSTERVERSIONINFO structure


## -description


Describes 
    information about the version of the <a href="https://msdn.microsoft.com/90717d6e-f2a4-49a0-86b6-17de1c4bcfe4">Cluster service</a> 
    installed locally on a <a href="https://msdn.microsoft.com/4381e378-7bf2-4dbc-b56e-3fed33193d32">node</a>.


## -struct-fields




### -field dwVersionInfoSize

Size, in bytes, of the data structure. Users must set this size prior to calling 
      <a href="https://msdn.microsoft.com/5b259eb9-c5d0-4f4f-8a6b-14eaed716612">GetClusterInformation</a>.


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
      node can join to form a <a href="https://msdn.microsoft.com/library/windows/hardware/dn922625">cluster</a>.


### -field dwClusterLowestVersion

Identifies the lowest version of the Cluster service with which the Cluster service installed on the local 
      node can join to form a cluster.


### -field dwFlags

If the cluster nodes are running different versions of the Cluster service, this value is set to 
      <b>CLUSTER_VERSION_FLAG_MIXED_MODE</b>. If all cluster nodes are running the same version of 
      the <a href="https://msdn.microsoft.com/90717d6e-f2a4-49a0-86b6-17de1c4bcfe4">Cluster service</a>, this value is 0.


### -field dwReserved

This value is reserved for internal use.


## -remarks



To obtain cluster version information, applications declare a 
    <b>CLUSTERVERSIONINFO</b> structure, specify the size of the 
    structure in the <b>dwVersionInfoSize</b> member, and call the 
    <a href="https://msdn.microsoft.com/5b259eb9-c5d0-4f4f-8a6b-14eaed716612">GetClusterInformation</a> function. 
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
    <a href="https://msdn.microsoft.com/919345fa-cbaa-4d01-bd3c-9ca69cab5094">Version Compatibility</a>.




## -see-also




<a href="https://msdn.microsoft.com/5b259eb9-c5d0-4f4f-8a6b-14eaed716612">GetClusterInformation</a>
 

 

