---
UID: NE:clusapi.CLUS_RESSUBCLASS_NETWORK
title: CLUS_RESSUBCLASS_NETWORK
author: windows-sdk-content
description: Identifies a resource subclass that manages an IP address provider.
old-location: mscs\clus_ressubclass_network.htm
old-project: mscs
ms.assetid: 1dea2545-f0d4-4730-87af-19de135c1640
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: CLUS_RESSUBCLASS_NETWORK, CLUS_RESSUBCLASS_NETWORK enumeration [Failover Cluster], CLUS_RESSUBCLASS_NETWORK_INTERNET_PROTOCOL, clusapi/CLUS_RESSUBCLASS_NETWORK, clusapi/CLUS_RESSUBCLASS_NETWORK_INTERNET_PROTOCOL, msclus/CLUS_RESSUBCLASS_NETWORK, msclus/CLUS_RESSUBCLASS_NETWORK_INTERNET_PROTOCOL, mscs.clus_ressubclass_network
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: clusapi.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: CLUS_RESSUBCLASS_NETWORK
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
req.lib: 
req.dll: 
req.irql: 
---

# CLUS_RESSUBCLASS_NETWORK enumeration


## -description


Identifies a resource subclass that manages an IP address provider.


## -enum-fields




### -field CLUS_RESSUBCLASS_NETWORK_INTERNET_PROTOCOL

Identifies a resource subclass that manages an IP address provider. The 
      <a href="https://msdn.microsoft.com/a98ca55a-6535-48cf-a925-5005baa01b94">ClusterResourceControl</a> function with the 
      <a href="https://msdn.microsoft.com/4c4f8809-d6eb-43e1-a09e-cfe3770a1fd4">CLUSCTL_RESOURCE_GET_CLASS_INFO</a> 
      control code can retrieve a 
      <a href="https://msdn.microsoft.com/b8b6c479-2e35-4cc9-b864-d495c3bded25">CLUS_RESOURCE_CLASS_INFO</a> structure that contains 
      this information.


## -see-also




<a href="https://msdn.microsoft.com/4c4f8809-d6eb-43e1-a09e-cfe3770a1fd4">CLUSCTL_RESOURCE_GET_CLASS_INFO</a>



<a href="https://msdn.microsoft.com/b8b6c479-2e35-4cc9-b864-d495c3bded25">CLUS_RESOURCE_CLASS_INFO</a>



<a href="https://msdn.microsoft.com/a98ca55a-6535-48cf-a925-5005baa01b94">ClusterResourceControl</a>
 

 

