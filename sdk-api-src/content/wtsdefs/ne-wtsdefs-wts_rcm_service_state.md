---
UID: NE:wtsdefs.WTS_RCM_SERVICE_STATE
title: WTS_RCM_SERVICE_STATE
author: windows-sdk-content
description: Contains information about the state of the Remote Desktop Services service.
old-location: termserv\wts_rcm_service_state.htm
tech.root: termserv
ms.assetid: 5f022d92-b048-4c87-918c-6e8f297cc1a6
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: WRDS_RCM_SERVICE_STATE, WRDS_RCM_SERVICE_STATE enumeration [Remote Desktop Services], WTS_RCM_SERVICE_STATE, WTS_RCM_SERVICE_STATE enumeration [Remote Desktop Services], WTS_SERVICE_NONE, WTS_SERVICE_START, WTS_SERVICE_STOP, termserv.wts_rcm_service_state, wtsdefs/WRDS_RCM_SERVICE_STATE, wtsdefs/WTS_RCM_SERVICE_STATE, wtsdefs/WTS_SERVICE_NONE, wtsdefs/WTS_SERVICE_START, wtsdefs/WTS_SERVICE_STOP
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wtsdefs.h
api_name:
 - WTS_RCM_SERVICE_STATE
product: Windows
targetos: Windows
req.typenames: WTS_RCM_SERVICE_STATE
req.redist: 
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



This enumeration type is used by the <a href="https://msdn.microsoft.com/5f4469f5-5a64-4292-bbe6-cc030f1421f5">WTS_SERVICE_STATE</a> structure.



