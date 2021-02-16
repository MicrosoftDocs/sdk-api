---
UID: NS:wtsdefs._WTS_SERVICE_STATE
title: WTS_SERVICE_STATE (wtsdefs.h)
description: Contains information about changes in the state of the Remote Desktop Services service.
helpviewer_keywords: ["*PWTS_SERVICE_STATE","PWRDS_SERVICE_STATE","PWRDS_SERVICE_STATE structure pointer [Remote Desktop Services]","PWTS_SERVICE_STATE","PWTS_SERVICE_STATE structure pointer [Remote Desktop Services]","WRDS_SERVICE_STATE","WRDS_SERVICE_STATE structure [Remote Desktop Services]","WTS_SERVICE_STATE","WTS_SERVICE_STATE structure [Remote Desktop Services]","termserv.wts_service_state","wtsdefs/PWRDS_SERVICE_STATE","wtsdefs/PWTS_SERVICE_STATE","wtsdefs/WRDS_SERVICE_STATE","wtsdefs/WTS_SERVICE_STATE"]
old-location: termserv\wts_service_state.htm
tech.root: TermServ
ms.assetid: 5f4469f5-5a64-4292-bbe6-cc030f1421f5
ms.date: 12/05/2018
ms.keywords: '*PWTS_SERVICE_STATE, PWRDS_SERVICE_STATE, PWRDS_SERVICE_STATE structure pointer [Remote Desktop Services], PWTS_SERVICE_STATE, PWTS_SERVICE_STATE structure pointer [Remote Desktop Services], WRDS_SERVICE_STATE, WRDS_SERVICE_STATE structure [Remote Desktop Services], WTS_SERVICE_STATE, WTS_SERVICE_STATE structure [Remote Desktop Services], termserv.wts_service_state, wtsdefs/PWRDS_SERVICE_STATE, wtsdefs/PWTS_SERVICE_STATE, wtsdefs/WRDS_SERVICE_STATE, wtsdefs/WTS_SERVICE_STATE'
req.header: wtsdefs.h
req.include-header: Wtsprotocol.h
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 R2
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
req.typenames: WTS_SERVICE_STATE, *PWTS_SERVICE_STATE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WTS_SERVICE_STATE
 - wtsdefs/_WTS_SERVICE_STATE
 - PWTS_SERVICE_STATE
 - wtsdefs/PWTS_SERVICE_STATE
 - WTS_SERVICE_STATE
 - wtsdefs/WTS_SERVICE_STATE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wtsdefs.h
api_name:
 - WTS_SERVICE_STATE
---

# WTS_SERVICE_STATE structure


## -description

Contains information about changes in the state of the Remote Desktop Services service.

## -struct-fields

### -field RcmServiceState

A value of the <a href="/windows/desktop/api/wtsdefs/ne-wtsdefs-wts_rcm_service_state">WTS_RCM_SERVICE_STATE</a> enumeration type that specifies whether the service is starting or stopping.

### -field RcmDrainState

A value of the <a href="/windows/desktop/api/wtsdefs/ne-wtsdefs-wts_rcm_drain_state">WTS_RCM_DRAIN_STATE</a> enumeration type that specifies whether the  RD Session Host server is changing its drain state.

## -remarks

This structure is used by the <a href="/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwtsprotocolmanager-notifyservicestatechange">NotifyServiceStateChange</a> method.