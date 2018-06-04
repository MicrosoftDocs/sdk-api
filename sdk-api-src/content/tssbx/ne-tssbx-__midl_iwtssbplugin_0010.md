---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# __MIDL_IWTSSBPlugin_0010 enumeration


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
 

 

