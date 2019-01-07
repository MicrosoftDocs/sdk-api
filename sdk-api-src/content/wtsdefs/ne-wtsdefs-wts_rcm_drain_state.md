---
UID: NE:wtsdefs.__unnamed_enum_1
title: WTS_RCM_DRAIN_STATE
author: windows-sdk-content
description: Contains information about the drain state of the Remote Desktop Session Host (RD Session Host) server.
old-location: termserv\wts_rcm_drain_state.htm
tech.root: termserv
ms.assetid: bb033bef-e325-42d0-8879-9a2151e43e91
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: WRDS_RCM_DRAIN_STATE, WRDS_RCM_DRAIN_STATE enumeration [Remote Desktop Services], WTS_DRAIN_IN_DRAIN, WTS_DRAIN_NOT_IN_DRAIN, WTS_DRAIN_STATE_NONE, WTS_RCM_DRAIN_STATE, WTS_RCM_DRAIN_STATE enumeration [Remote Desktop Services], termserv.wts_rcm_drain_state, wtsdefs/WRDS_RCM_DRAIN_STATE, wtsdefs/WTS_DRAIN_IN_DRAIN, wtsdefs/WTS_DRAIN_NOT_IN_DRAIN, wtsdefs/WTS_DRAIN_STATE_NONE, wtsdefs/WTS_RCM_DRAIN_STATE
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
 - WTS_RCM_DRAIN_STATE
product: Windows
targetos: Windows
req.typenames: WTS_RCM_DRAIN_STATE
req.redist: 
---

# WTS_RCM_DRAIN_STATE enumeration


## -description


Contains information about the drain state of the Remote Desktop Session Host (RD Session Host) server. A server in drain mode will not accept new connections, but it will reconnect users to existing sessions.


## -enum-fields




### -field WTS_DRAIN_STATE_NONE

There has been no change in the drain state.


### -field WTS_DRAIN_IN_DRAIN

The server is in drain mode, or it is entering drain mode. (It is not accepting new connections.)


### -field WTS_DRAIN_NOT_IN_DRAIN

The server is not in drain mode, or it is exiting drain mode. (It is accepting new connections.)


## -remarks



This enumeration type is used by the <a href="https://msdn.microsoft.com/5f4469f5-5a64-4292-bbe6-cc030f1421f5">WTS_SERVICE_STATE</a> structure.



