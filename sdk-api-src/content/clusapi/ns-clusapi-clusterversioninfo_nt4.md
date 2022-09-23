---
UID: NS:clusapi.CLUSTERVERSIONINFO_NT4
title: CLUSTERVERSIONINFO_NT4 (clusapi.h)
description: The CLUSTERVERSIONINFO_NT4 (clusapi.h) structure relates to multiple field types, with more information is to be determined.
helpviewer_keywords: ["*PCLUSTERVERSIONINFO_NT4","CLUSTERVERSIONINFO_NT4","CLUSTERVERSIONINFO_NT4 structure [Failover Cluster]","PCLUSTERVERSIONINFO_NT4","PCLUSTERVERSIONINFO_NT4 structure pointer [Failover Cluster]","clusapi/CLUSTERVERSIONINFO_NT4","clusapi/PCLUSTERVERSIONINFO_NT4","mscs.clusterversioninfo_nt4"]
old-location: mscs\clusterversioninfo_nt4.htm
tech.root: MsCS
ms.assetid: 1420C1B9-3361-4D7C-B968-34967C0818F4
ms.date: 08/03/2022
ms.keywords: '*PCLUSTERVERSIONINFO_NT4, CLUSTERVERSIONINFO_NT4, CLUSTERVERSIONINFO_NT4 structure [Failover Cluster], PCLUSTERVERSIONINFO_NT4, PCLUSTERVERSIONINFO_NT4 structure pointer [Failover Cluster], clusapi/CLUSTERVERSIONINFO_NT4, clusapi/PCLUSTERVERSIONINFO_NT4, mscs.clusterversioninfo_nt4'
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
req.typenames: CLUSTERVERSIONINFO_NT4, *PCLUSTERVERSIONINFO_NT4
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CLUSTERVERSIONINFO_NT4
 - clusapi/CLUSTERVERSIONINFO_NT4
 - PCLUSTERVERSIONINFO_NT4
 - clusapi/PCLUSTERVERSIONINFO_NT4
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
 - CLUSTERVERSIONINFO_NT4
---

# CLUSTERVERSIONINFO_NT4 structure


## -description

TBD

## -struct-fields

### -field dwVersionInfoSize

Contains the  size, in bytes, of the data structure. Users must set this size prior to calling the  
      <a href="/windows/desktop/api/clusapi/nf-clusapi-getclusterinformation">GetClusterInformation</a>   function.

### -field MajorVersion

Identifies the major version number of the operating system that is  installed on the local node. For example, for 
      version X.Y, the major version number is X.

### -field MinorVersion

Identifies the minor version number of the operating system that is  installed on the local node. For example, for 
      version X.Y, the minor version number is Y.

### -field BuildNumber

Identifies the build number of the operating system that is  installed on the local node, such as 224.

### -field szVendorId

Contains the vendor identifier information for the cluster service that is  installed on the local node.

### -field szCSDVersion

Contains the latest service pack that is  installed on the node. If a Service Pack is not installed, the 
      <b>szCSDVersion</b> member is empty.

## -see-also

<a href="/previous-versions/windows/desktop/mscs/utility-structures">Utility Structures</a>
