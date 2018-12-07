---
UID: NS:wcmapi._WCM_USAGE_DATA
title: "_WCM_USAGE_DATA"
author: windows-sdk-content
description: Contains information related to connection usage.
old-location: wcm\wcm_usage_data.htm
tech.root: wcm
ms.assetid: c6a483cf-d392-495f-854d-ccc782b30aa5
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PWCM_USAGE_DATA, PWCM_USAGE_DATA, PWCM_USAGE_DATA structure pointer [Windows Connection Manager], WCM_USAGE_DATA, WCM_USAGE_DATA structure [Windows Connection Manager], _WCM_USAGE_DATA, wcm.wcm_usage_data, wcmapi/PWCM_USAGE_DATA, wcmapi/WCM_USAGE_DATA"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wcmapi.h
api_name:
 - WCM_USAGE_DATA
product: Windows
targetos: Windows
req.typenames: WCM_USAGE_DATA, *PWCM_USAGE_DATA
req.redist: 
---

# _WCM_USAGE_DATA structure


## -description


The <b>WCM_USAGE_DATA</b> structure contains information related to connection  usage.


## -struct-fields




### -field UsageInMegabytes

Type: <b>DWORD</b>

The connection usage, in megabytes.


### -field LastSyncTime

Type: <b>FILETIME</b>

Specifies the last time that usage information was reconciled with the carrier's billing system.

