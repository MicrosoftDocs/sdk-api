---
UID: NS:wtsdefs._WTS_SERVICE_STATE
title: "_WTS_SERVICE_STATE"
author: windows-sdk-content
description: Contains information about changes in the state of the Remote Desktop Services service.
old-location: termserv\wts_service_state.htm
old-project: TermServ
ms.assetid: 5f4469f5-5a64-4292-bbe6-cc030f1421f5
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: "*PWTS_SERVICE_STATE, PWRDS_SERVICE_STATE, PWRDS_SERVICE_STATE structure pointer [Remote Desktop Services], PWTS_SERVICE_STATE, PWTS_SERVICE_STATE structure pointer [Remote Desktop Services], WRDS_SERVICE_STATE, WRDS_SERVICE_STATE structure [Remote Desktop Services], WTS_SERVICE_STATE, WTS_SERVICE_STATE structure [Remote Desktop Services], _WTS_SERVICE_STATE, termserv.wts_service_state, wtsdefs/PWRDS_SERVICE_STATE, wtsdefs/PWTS_SERVICE_STATE, wtsdefs/WRDS_SERVICE_STATE, wtsdefs/WTS_SERVICE_STATE"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
tech.root: 
req.typenames: WTS_SERVICE_STATE, *PWTS_SERVICE_STATE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wtsdefs.h
api_name:
 - WTS_SERVICE_STATE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# _WTS_SERVICE_STATE structure


## -description


Contains information about changes in the state of the Remote Desktop Services service.


## -struct-fields




### -field RcmServiceState

A value of the <a href="https://msdn.microsoft.com/5f022d92-b048-4c87-918c-6e8f297cc1a6">WTS_RCM_SERVICE_STATE</a> enumeration type that specifies whether the service is starting or stopping.


### -field RcmDrainState

A value of the <a href="https://msdn.microsoft.com/bb033bef-e325-42d0-8879-9a2151e43e91">WTS_RCM_DRAIN_STATE</a> enumeration type that specifies whether the  RD Session Host server is changing its drain state.


## -remarks



This structure is used by the <a href="https://msdn.microsoft.com/303a53b3-b297-486c-9422-706ec60441f2">NotifyServiceStateChange</a> method.



