---
UID: NS:clusapi.CLUSTERVERSIONINFO_NT4
title: CLUSTERVERSIONINFO_NT4
author: windows-driver-content
description: TBD.
old-location: mscs\clusterversioninfo_nt4.htm
old-project: MsCS
ms.assetid: 1420C1B9-3361-4D7C-B968-34967C0818F4
ms.author: windowsdriverdev
ms.date: 4/24/2018
ms.keywords: "*PCLUSTERVERSIONINFO_NT4, CLUSTERVERSIONINFO_NT4, CLUSTERVERSIONINFO_NT4 structure [Failover Cluster], PCLUSTERVERSIONINFO_NT4, PCLUSTERVERSIONINFO_NT4 structure pointer [Failover Cluster], clusapi/CLUSTERVERSIONINFO_NT4, clusapi/PCLUSTERVERSIONINFO_NT4, mscs.clusterversioninfo_nt4"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
req.typenames: CLUSTERVERSIONINFO_NT4, *PCLUSTERVERSIONINFO_NT4
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	ClusAPI.h
api_name:
-	CLUSTERVERSIONINFO_NT4
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# CLUSTERVERSIONINFO_NT4 structure


## -description


TBD


## -struct-fields




### -field dwVersionInfoSize

Contains the  size, in bytes, of the data structure. Users must set this size prior to calling the  
      <a href="https://msdn.microsoft.com/5b259eb9-c5d0-4f4f-8a6b-14eaed716612">GetClusterInformation</a>   function.


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




<a href="https://msdn.microsoft.com/45da8dbc-dd70-4f95-b933-66d8e4340448">Utility Structures</a>
 

 

