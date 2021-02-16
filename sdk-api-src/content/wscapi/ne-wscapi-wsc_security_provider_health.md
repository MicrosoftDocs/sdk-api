---
UID: NE:wscapi._WSC_SECURITY_PROVIDER_HEALTH
title: WSC_SECURITY_PROVIDER_HEALTH (wscapi.h)
description: Defines the possible states for any service monitored by Windows Security Center (WSC).
helpviewer_keywords: ["*PWSC_SECURITY_PROVIDER_HEALTH","WSC_SECURITY_PROVIDER_HEALTH","WSC_SECURITY_PROVIDER_HEALTH enumeration [Windows API]","WSC_SECURITY_PROVIDER_HEALTH","*PWSC_SECURITY_PROVIDER_HEALTH","WSC_SECURITY_PROVIDER_HEALTH","*PWSC_SECURITY_PROVIDER_HEALTH enumeration [Windows API]","WSC_SECURITY_PROVIDER_HEALTH_GOOD","WSC_SECURITY_PROVIDER_HEALTH_NOTMONITORED","WSC_SECURITY_PROVIDER_HEALTH_POOR","WSC_SECURITY_PROVIDER_HEALTH_SNOOZE","winprog.wsc_security_provider_health","wscapi/WSC_SECURITY_PROVIDER_HEALTH","wscapi/WSC_SECURITY_PROVIDER_HEALTH_GOOD","wscapi/WSC_SECURITY_PROVIDER_HEALTH_NOTMONITORED","wscapi/WSC_SECURITY_PROVIDER_HEALTH_POOR","wscapi/WSC_SECURITY_PROVIDER_HEALTH_SNOOZE"]
old-location: winprog\wsc_security_provider_health.htm
tech.root: winprog
ms.assetid: a5f34088-13b9-4269-a3ca-777e0bb9b655
ms.date: 12/05/2018
ms.keywords: '*PWSC_SECURITY_PROVIDER_HEALTH, WSC_SECURITY_PROVIDER_HEALTH, WSC_SECURITY_PROVIDER_HEALTH enumeration [Windows API], WSC_SECURITY_PROVIDER_HEALTH,*PWSC_SECURITY_PROVIDER_HEALTH, WSC_SECURITY_PROVIDER_HEALTH,*PWSC_SECURITY_PROVIDER_HEALTH enumeration [Windows API], WSC_SECURITY_PROVIDER_HEALTH_GOOD, WSC_SECURITY_PROVIDER_HEALTH_NOTMONITORED, WSC_SECURITY_PROVIDER_HEALTH_POOR, WSC_SECURITY_PROVIDER_HEALTH_SNOOZE, winprog.wsc_security_provider_health, wscapi/WSC_SECURITY_PROVIDER_HEALTH, wscapi/WSC_SECURITY_PROVIDER_HEALTH_GOOD, wscapi/WSC_SECURITY_PROVIDER_HEALTH_NOTMONITORED, wscapi/WSC_SECURITY_PROVIDER_HEALTH_POOR, wscapi/WSC_SECURITY_PROVIDER_HEALTH_SNOOZE'
req.header: wscapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: None supported
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
req.typenames: WSC_SECURITY_PROVIDER_HEALTH, *PWSC_SECURITY_PROVIDER_HEALTH
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WSC_SECURITY_PROVIDER_HEALTH
 - wscapi/_WSC_SECURITY_PROVIDER_HEALTH
 - PWSC_SECURITY_PROVIDER_HEALTH
 - wscapi/PWSC_SECURITY_PROVIDER_HEALTH
 - WSC_SECURITY_PROVIDER_HEALTH
 - wscapi/WSC_SECURITY_PROVIDER_HEALTH
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wscapi.h
api_name:
 - WSC_SECURITY_PROVIDER_HEALTH, *PWSC_SECURITY_PROVIDER_HEALTH
---

# WSC_SECURITY_PROVIDER_HEALTH enumeration


## -description

Defines the possible states for any service monitored by Windows Security Center (WSC).

## -enum-fields

### -field WSC_SECURITY_PROVIDER_HEALTH_GOOD

The status of the security provider category is good and does not need user attention.

### -field WSC_SECURITY_PROVIDER_HEALTH_NOTMONITORED

The status of the security provider category is not monitored by WSC.

### -field WSC_SECURITY_PROVIDER_HEALTH_POOR

The status of the security provider category is poor and the computer may be at risk.

### -field WSC_SECURITY_PROVIDER_HEALTH_SNOOZE

The security provider category is in snooze state. Snooze indicates that WSC is not actively protecting the computer.

## -see-also

<a href="/windows/desktop/api/wscapi/nf-wscapi-wscgetsecurityproviderhealth">WscGetSecurityProviderHealth</a>