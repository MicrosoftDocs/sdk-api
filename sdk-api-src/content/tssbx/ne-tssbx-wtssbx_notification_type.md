---
UID: NE:tssbx.__MIDL_IWTSSBPlugin_0010
title: WTSSBX_NOTIFICATION_TYPE (tssbx.h)
description: Contains values that indicate the type of status change that occurred on a Remote Desktop Session Host (RD Session Host) server or a user session.
helpviewer_keywords: ["WTSSBX_NOTIFICATION_ADDED","WTSSBX_NOTIFICATION_CHANGED","WTSSBX_NOTIFICATION_REMOVED","WTSSBX_NOTIFICATION_RESYNC","WTSSBX_NOTIFICATION_TYPE","WTSSBX_NOTIFICATION_TYPE enumeration [Remote Desktop Services]","termserv.wtssbx_notification_type","tssbx/WTSSBX_NOTIFICATION_ADDED","tssbx/WTSSBX_NOTIFICATION_CHANGED","tssbx/WTSSBX_NOTIFICATION_REMOVED","tssbx/WTSSBX_NOTIFICATION_RESYNC","tssbx/WTSSBX_NOTIFICATION_TYPE"]
old-location: termserv\wtssbx_notification_type.htm
tech.root: TermServ
ms.assetid: 06da6e20-a4de-4e2d-8f42-6d99b738226c
ms.date: 12/05/2018
ms.keywords: WTSSBX_NOTIFICATION_ADDED, WTSSBX_NOTIFICATION_CHANGED, WTSSBX_NOTIFICATION_REMOVED, WTSSBX_NOTIFICATION_RESYNC, WTSSBX_NOTIFICATION_TYPE, WTSSBX_NOTIFICATION_TYPE enumeration [Remote Desktop Services], termserv.wtssbx_notification_type, tssbx/WTSSBX_NOTIFICATION_ADDED, tssbx/WTSSBX_NOTIFICATION_CHANGED, tssbx/WTSSBX_NOTIFICATION_REMOVED, tssbx/WTSSBX_NOTIFICATION_RESYNC, tssbx/WTSSBX_NOTIFICATION_TYPE
req.header: tssbx.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Tssbx.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: WTSSBX_NOTIFICATION_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL_IWTSSBPlugin_0010
 - tssbx/__MIDL_IWTSSBPlugin_0010
 - WTSSBX_NOTIFICATION_TYPE
 - tssbx/WTSSBX_NOTIFICATION_TYPE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Tssbx.h
api_name:
 - WTSSBX_NOTIFICATION_TYPE
---

# WTSSBX_NOTIFICATION_TYPE enumeration


## -description

Contains values that indicate the type of status change that occurred on a Remote Desktop Session Host (RD Session Host) server or a user session. Remote Desktop Connection Broker (RD Connection Broker) uses this enumeration type in the <a href="/windows/desktop/api/tssbx/nf-tssbx-iwtssbplugin-wtssbx_machinechangenotification">WTSSBX_MachineChangeNotification</a> and <a href="/windows/desktop/api/tssbx/nf-tssbx-iwtssbplugin-wtssbx_sessionchangenotification">WTSSBX_SessionChangeNotification</a> methods to notify the plug-in about changes that have occurred.

## -enum-fields

### -field WTSSBX_NOTIFICATION_REMOVED:0x1

RD Connection Broker received a Removed notification. This indicates that a user has logged off an RD Session Host server or that an RD Session Host server left a farm in RD Connection Broker.

### -field WTSSBX_NOTIFICATION_CHANGED:0x2

RD Connection Broker received a Changed notification. This indicates that the session state of the RD Session Host server changed or that an RD Session Host server setting, such as the IP address or the maximum session limit, changed.

### -field WTSSBX_NOTIFICATION_ADDED:0x4

RD Connection Broker received  an Added notification. This indicates that a user logged into an RD Session Host server or that an RD Session Host server joined a  farm in RD Connection Broker.

### -field WTSSBX_NOTIFICATION_RESYNC:0x8

RD Connection Broker received a Resync notification. This indicates that an RD Session Host server joined a  farm in RD Connection Broker and the new RD Session Host server is now synchronizing its session information with the RD Connection Broker server.

## -see-also

<a href="/windows/desktop/api/tssbx/nn-tssbx-iwtssbplugin">IWTSSBPlugin</a>
