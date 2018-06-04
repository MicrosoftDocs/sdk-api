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

# _WCM_DATAPLAN_STATUS structure


## -description


The <b>WCM_DATAPLAN_STATUS</b> structure specifies subscription information for a network connection.


## -struct-fields




### -field UsageData

Type: <b><a href="https://msdn.microsoft.com/c6a483cf-d392-495f-854d-ccc782b30aa5">WCM_USAGE_DATA</a></b>

Contains usage data.


### -field DataLimitInMegabytes

Type: <b>DWORD</b>

Specifies the data limit, in megabytes.


### -field InboundBandwidthInKbps

Type: <b>DWORD</b>

Specifies the inbound bandwidth, in kilobits per second.


### -field OutboundBandwidthInKbps

Type: <b>DWORD</b>

Specifies the outbound bandwidth, in kilobits per second.


### -field BillingCycle

Type: <b><a href="https://msdn.microsoft.com/5cfcdfb7-aa33-4582-ba17-e1a305b830f5">WCM_BILLING_CYCLE_INFO</a></b>

Contains information about the billing cycle.


### -field MaxTransferSizeInMegabytes

Type: <b>DWORD</b>

Specifies the maximum size of a file that can be transferred, in megabytes.


### -field Reserved

Type: <b>DWORD</b>

Reserved.


## -see-also




<a href="https://msdn.microsoft.com/5cfcdfb7-aa33-4582-ba17-e1a305b830f5">WCM_BILLING_CYCLE_INFO</a>



<a href="https://msdn.microsoft.com/c6a483cf-d392-495f-854d-ccc782b30aa5">WCM_USAGE_DATA</a>
 

 

