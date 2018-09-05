---
UID: NS:wcmapi._WCM_DATAPLAN_STATUS
title: "_WCM_DATAPLAN_STATUS"
author: windows-sdk-content
description: Specifies subscription information for a network connection.
old-location: wcm\wcm_dataplan_status.htm
old-project: wcm
ms.assetid: 6ed0f05c-a9f8-49bb-9fb0-b91af8594d76
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: "*PWCM_DATAPLAN_STATUS, PWCM_DATAPLAN_STATUS, PWCM_DATAPLAN_STATUS structure pointer [Windows Connection Manager], WCM_DATAPLAN_STATUS, WCM_DATAPLAN_STATUS structure [Windows Connection Manager], _WCM_DATAPLAN_STATUS, wcm.wcm_dataplan_status, wcmapi/PWCM_DATAPLAN_STATUS, wcmapi/WCM_DATAPLAN_STATUS"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: wcmapi.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
req.typenames: WCM_DATAPLAN_STATUS, *PWCM_DATAPLAN_STATUS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wcmapi.h
api_name:
 - WCM_DATAPLAN_STATUS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
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
 

 

