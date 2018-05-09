---
UID: NS:clusapi.RESOURCE_FAILURE_INFO_BUFFER
title: RESOURCE_FAILURE_INFO_BUFFER
author: windows-driver-content
description: Represents a buffer for a resource failure.
old-location: mscs\resource_failure_info_buffer.htm
old-project: MsCS
ms.assetid: 131EEF4A-DB1E-4FF7-8329-4AA422AB83B0
ms.author: windowsdriverdev
ms.date: 5/7/2018
ms.keywords: "*PRESOURCE_FAILURE_INFO_BUFFER, PRESOURCE_FAILURE_INFO_BUFFER, PRESOURCE_FAILURE_INFO_BUFFER structure pointer [Failover Cluster], RESOURCE_FAILURE_INFO_BUFFER, RESOURCE_FAILURE_INFO_BUFFER structure [Failover Cluster], clusapi/PRESOURCE_FAILURE_INFO_BUFFER, clusapi/RESOURCE_FAILURE_INFO_BUFFER, msclus/PRESOURCE_FAILURE_INFO_BUFFER, msclus/RESOURCE_FAILURE_INFO_BUFFER, mscs.resource_failure_info_buffer"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: clusapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2012
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: RESOURCE_FAILURE_INFO_BUFFER, *PRESOURCE_FAILURE_INFO_BUFFER
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	ClusApi.h
-	MSClus.h
api_name:
-	RESOURCE_FAILURE_INFO_BUFFER
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# RESOURCE_FAILURE_INFO_BUFFER structure


## -description


Represents a buffer for a resource failure.


## -struct-fields




### -field dwVersion

The version of this structure. Set this parameter to <b>RESOURCE_FAILURE_INFO_VERSION_1</b> (0x1).


### -field Info

The <a href="https://msdn.microsoft.com/3FE0CC0E-B097-48FC-882F-F6B236BB0CCB">RESOURCE_FAILURE_INFO</a> structure that contains information about the failover attempts for the resource failure.


## -see-also




<a href="https://msdn.microsoft.com/45da8dbc-dd70-4f95-b933-66d8e4340448">Utility structures</a>
 

 

