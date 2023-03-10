---
UID: NE:wtsdefs.WTS_RCM_SERVICE_STATE
title: WTS_RCM_SERVICE_STATE (wtsdefs.h)
description: Contains information about the state of the Remote Desktop Services service.
helpviewer_keywords: ["WRDS_RCM_SERVICE_STATE","WRDS_RCM_SERVICE_STATE enumeration [Remote Desktop Services]","WTS_RCM_SERVICE_STATE","WTS_RCM_SERVICE_STATE enumeration [Remote Desktop Services]","WTS_SERVICE_NONE","WTS_SERVICE_START","WTS_SERVICE_STOP","termserv.wts_rcm_service_state","wtsdefs/WRDS_RCM_SERVICE_STATE","wtsdefs/WTS_RCM_SERVICE_STATE","wtsdefs/WTS_SERVICE_NONE","wtsdefs/WTS_SERVICE_START","wtsdefs/WTS_SERVICE_STOP"]
old-location: termserv\wts_rcm_service_state.htm
tech.root: TermServ
ms.assetid: 5f022d92-b048-4c87-918c-6e8f297cc1a6
ms.date: 12/05/2018
ms.keywords: WRDS_RCM_SERVICE_STATE, WRDS_RCM_SERVICE_STATE enumeration [Remote Desktop Services], WTS_RCM_SERVICE_STATE, WTS_RCM_SERVICE_STATE enumeration [Remote Desktop Services], WTS_SERVICE_NONE, WTS_SERVICE_START, WTS_SERVICE_STOP, termserv.wts_rcm_service_state, wtsdefs/WRDS_RCM_SERVICE_STATE, wtsdefs/WTS_RCM_SERVICE_STATE, wtsdefs/WTS_SERVICE_NONE, wtsdefs/WTS_SERVICE_START, wtsdefs/WTS_SERVICE_STOP
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
req.typenames: WTS_RCM_SERVICE_STATE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WTS_RCM_SERVICE_STATE
 - wtsdefs/WTS_RCM_SERVICE_STATE
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
 - WTS_RCM_SERVICE_STATE
---

# WTS_RCM_SERVICE_STATE enumeration


## -description

Contains information about the state of the Remote Desktop Services service.

## -enum-fields

### -field WTS_SERVICE_NONE

There has been no change in the state of the service.

### -field WTS_SERVICE_START

The RCM service is starting.

### -field WTS_SERVICE_STOP

The RCM service is stopping.

## -remarks

This enumeration type is used by the <a href="/windows/desktop/api/wtsdefs/ns-wtsdefs-wts_service_state">WTS_SERVICE_STATE</a> structure.

