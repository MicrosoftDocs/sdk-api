---
UID: NS:wcmapi.WCM_BILLING_CYCLE_INFO
title: WCM_BILLING_CYCLE_INFO (wcmapi.h)
description: Specifies information about the billing cycle.
helpviewer_keywords: ["WCM_BILLING_CYCLE_INFO","WCM_BILLING_CYCLE_INFO structure [Windows Connection Manager]","wcm.wcm_billing_cycle_info","wcmapi/WCM_BILLING_CYCLE_INFO"]
old-location: wcm\wcm_billing_cycle_info.htm
tech.root: wcm
ms.assetid: 5cfcdfb7-aa33-4582-ba17-e1a305b830f5
ms.date: 12/05/2018
ms.keywords: WCM_BILLING_CYCLE_INFO, WCM_BILLING_CYCLE_INFO structure [Windows Connection Manager], wcm.wcm_billing_cycle_info, wcmapi/WCM_BILLING_CYCLE_INFO
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
req.typenames: WCM_BILLING_CYCLE_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WCM_BILLING_CYCLE_INFO
 - wcmapi/WCM_BILLING_CYCLE_INFO
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
 - WCM_BILLING_CYCLE_INFO
---

# WCM_BILLING_CYCLE_INFO structure


## -description

The <b>WCM_BILLING_CYCLE_INFO</b> structure specifies information about the billing cycle.

## -struct-fields

### -field StartDate

Type: <b>FILETIME</b>

Specifies the start date of the cycle.

### -field Duration

Type: <b><a href="/windows/desktop/api/wcmapi/ns-wcmapi-wcm_time_interval">WCM_TIME_INTERVAL</a></b>

Specifies the billing cycle duration.

### -field Reset

Type: <b>BOOL</b>

True if at the end of the billing cycle, a new billing cycle of the same duration will start. False if the service will terminate at the end of the billing cycle.

## -see-also

<a href="/windows/desktop/api/wcmapi/ns-wcmapi-wcm_time_interval">WCM_TIME_INTERVAL</a>