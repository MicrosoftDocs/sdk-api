---
UID: NS:wcmapi._WCM_DATAPLAN_STATUS
title: WCM_DATAPLAN_STATUS (wcmapi.h)
description: Specifies subscription information for a network connection.
helpviewer_keywords: ["*PWCM_DATAPLAN_STATUS","PWCM_DATAPLAN_STATUS","PWCM_DATAPLAN_STATUS structure pointer [Windows Connection Manager]","WCM_DATAPLAN_STATUS","WCM_DATAPLAN_STATUS structure [Windows Connection Manager]","wcm.wcm_dataplan_status","wcmapi/PWCM_DATAPLAN_STATUS","wcmapi/WCM_DATAPLAN_STATUS"]
old-location: wcm\wcm_dataplan_status.htm
tech.root: wcm
ms.assetid: 6ed0f05c-a9f8-49bb-9fb0-b91af8594d76
ms.date: 12/05/2018
ms.keywords: '*PWCM_DATAPLAN_STATUS, PWCM_DATAPLAN_STATUS, PWCM_DATAPLAN_STATUS structure pointer [Windows Connection Manager], WCM_DATAPLAN_STATUS, WCM_DATAPLAN_STATUS structure [Windows Connection Manager], wcm.wcm_dataplan_status, wcmapi/PWCM_DATAPLAN_STATUS, wcmapi/WCM_DATAPLAN_STATUS'
req.header: wcmapi.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: WCM_DATAPLAN_STATUS, *PWCM_DATAPLAN_STATUS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WCM_DATAPLAN_STATUS
 - wcmapi/_WCM_DATAPLAN_STATUS
 - PWCM_DATAPLAN_STATUS
 - wcmapi/PWCM_DATAPLAN_STATUS
 - WCM_DATAPLAN_STATUS
 - wcmapi/WCM_DATAPLAN_STATUS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wcmapi.h
api_name:
 - WCM_DATAPLAN_STATUS
---

# WCM_DATAPLAN_STATUS structure


## -description

The <b>WCM_DATAPLAN_STATUS</b> structure specifies subscription information for a network connection.

## -struct-fields

### -field UsageData

Type: <b><a href="/windows/desktop/api/wcmapi/ns-wcmapi-wcm_usage_data">WCM_USAGE_DATA</a></b>

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

Type: <b><a href="/windows/desktop/api/wcmapi/ns-wcmapi-wcm_billing_cycle_info">WCM_BILLING_CYCLE_INFO</a></b>

Contains information about the billing cycle.

### -field MaxTransferSizeInMegabytes

Type: <b>DWORD</b>

Specifies the maximum size of a file that can be transferred, in megabytes.

### -field Reserved

Type: <b>DWORD</b>

Reserved.

## -see-also

<a href="/windows/desktop/api/wcmapi/ns-wcmapi-wcm_billing_cycle_info">WCM_BILLING_CYCLE_INFO</a>



<a href="/windows/desktop/api/wcmapi/ns-wcmapi-wcm_usage_data">WCM_USAGE_DATA</a>