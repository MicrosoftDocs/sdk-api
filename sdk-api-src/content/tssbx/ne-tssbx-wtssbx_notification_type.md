---
UID: NE:tssbx.__MIDL_IWTSSBPlugin_0010
title: WTSSBX_NOTIFICATION_TYPE
author: windows-sdk-content
description: Contains values that indicate the type of status change that occurred on a Remote Desktop Session Host (RD Session Host) server or a user session.
old-location: termserv\wtssbx_notification_type.htm
tech.root: TermServ
ms.assetid: 06da6e20-a4de-4e2d-8f42-6d99b738226c
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: WTSSBX_NOTIFICATION_ADDED, WTSSBX_NOTIFICATION_CHANGED, WTSSBX_NOTIFICATION_REMOVED, WTSSBX_NOTIFICATION_RESYNC, WTSSBX_NOTIFICATION_TYPE, WTSSBX_NOTIFICATION_TYPE enumeration [Remote Desktop Services], termserv.wtssbx_notification_type, tssbx/WTSSBX_NOTIFICATION_ADDED, tssbx/WTSSBX_NOTIFICATION_CHANGED, tssbx/WTSSBX_NOTIFICATION_REMOVED, tssbx/WTSSBX_NOTIFICATION_RESYNC, tssbx/WTSSBX_NOTIFICATION_TYPE
ms.topic: enum
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Tssbx.h
api_name:
 - WTSSBX_NOTIFICATION_TYPE
product: Windows
targetos: Windows
req.typenames: WTSSBX_NOTIFICATION_TYPE
req.redist: 
---

# WTSSBX_NOTIFICATION_TYPE enumeration


## -description


Contains values that indicate the type of status change that occurred on a Remote Desktop Session Host (RD Session Host) server or a user session. Remote Desktop Connection Broker (RD Connection Broker) uses this enumeration type in the <a href="https://msdn.microsoft.com/226ca68e-6c3d-4160-a569-ca0b92cb9316">WTSSBX_MachineChangeNotification</a> and <a href="https://msdn.microsoft.com/00426aa2-1d22-462f-9ad1-2a63d151493d">WTSSBX_SessionChangeNotification</a> methods to notify the plug-in about changes that have occurred.


## -enum-fields




### -field WTSSBX_NOTIFICATION_REMOVED

RD Connection Broker received a Removed notification. This indicates that a user has logged off an RD Session Host server or that an RD Session Host server left a farm in RD Connection Broker.


### -field WTSSBX_NOTIFICATION_CHANGED

RD Connection Broker received a Changed notification. This indicates that the session state of the RD Session Host server changed or that an RD Session Host server setting, such as the IP address or the maximum session limit, changed.


### -field WTSSBX_NOTIFICATION_ADDED

RD Connection Broker received  an Added notification. This indicates that a user logged into an RD Session Host server or that an RD Session Host server joined a  farm in RD Connection Broker.


### -field WTSSBX_NOTIFICATION_RESYNC

RD Connection Broker received a Resync notification. This indicates that an RD Session Host server joined a  farm in RD Connection Broker and the new RD Session Host server is now synchronizing its session information with the RD Connection Broker server.


## -see-also




<a href="https://msdn.microsoft.com/f6959b8c-a8a8-438b-8b6d-31bf0e782bac">IWTSSBPlugin</a>
 

 

