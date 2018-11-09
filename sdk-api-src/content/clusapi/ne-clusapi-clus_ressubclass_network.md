---
UID: NE:clusapi.CLUS_RESSUBCLASS_NETWORK
title: CLUS_RESSUBCLASS_NETWORK
author: windows-sdk-content
description: Identifies a resource subclass that manages an IP address provider.
old-location: mscs\clus_ressubclass_network.htm
tech.root: mscs
ms.assetid: 1dea2545-f0d4-4730-87af-19de135c1640
ms.author: windowssdkdev
ms.date: 11/06/2018
ms.keywords: CLUS_RESSUBCLASS_NETWORK, CLUS_RESSUBCLASS_NETWORK enumeration [Failover Cluster], CLUS_RESSUBCLASS_NETWORK_INTERNET_PROTOCOL, clusapi/CLUS_RESSUBCLASS_NETWORK, clusapi/CLUS_RESSUBCLASS_NETWORK_INTERNET_PROTOCOL, msclus/CLUS_RESSUBCLASS_NETWORK, msclus/CLUS_RESSUBCLASS_NETWORK_INTERNET_PROTOCOL, mscs.clus_ressubclass_network
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
 - MsClus.h
api_name:
 - CLUS_RESSUBCLASS_NETWORK
product: Windows
targetos: Windows
req.typenames: CLUS_RESSUBCLASS_NETWORK
req.redist: 
---

# CLUS_RESSUBCLASS_NETWORK enumeration


## -description


Identifies a resource subclass that manages an IP address provider.


## -enum-fields




### -field CLUS_RESSUBCLASS_NETWORK_INTERNET_PROTOCOL

Identifies a resource subclass that manages an IP address provider. The 
      <a href="https://msdn.microsoft.com/en-us/library/Aa369016(v=VS.85).aspx">ClusterResourceControl</a> function with the 
      <a href="https://msdn.microsoft.com/en-us/library/Aa367467(v=VS.85).aspx">CLUSCTL_RESOURCE_GET_CLASS_INFO</a> 
      control code can retrieve a 
      <a href="https://msdn.microsoft.com/en-us/library/Aa369187(v=VS.85).aspx">CLUS_RESOURCE_CLASS_INFO</a> structure that contains 
      this information.


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa367467(v=VS.85).aspx">CLUSCTL_RESOURCE_GET_CLASS_INFO</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa369187(v=VS.85).aspx">CLUS_RESOURCE_CLASS_INFO</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa369016(v=VS.85).aspx">ClusterResourceControl</a>
 

 

