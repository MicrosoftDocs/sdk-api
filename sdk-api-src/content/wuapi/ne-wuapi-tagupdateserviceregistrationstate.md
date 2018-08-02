---
UID: NE:wuapi.tagUpdateServiceRegistrationState
title: tagUpdateServiceRegistrationState
author: windows-sdk-content
description: Defines the possible states for an update service.
old-location: wua\updateserviceregistrationstate.htm
old-project: Wua_Sdk
ms.assetid: 798d1392-a8dc-4063-b33d-159a507161f1
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: UpdateServiceRegistrationState, UpdateServiceRegistrationState enumeration [Windows Update Agent], tagUpdateServiceRegistrationState, usrsNotRegistered, usrsRegistered, usrsRegistrationPending, wua.updateserviceregistrationstate, wuapi/UpdateServiceRegistrationState, wuapi/usrsNotRegistered, wuapi/usrsRegistered, wuapi/usrsRegistrationPending
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: wuapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP, Windows 2000 Professional with SP3 [desktop apps only]
req.target-min-winversvr: Windows Server 2003, Windows 2000 Server with SP3 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wuapi.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: UpdateServiceRegistrationState
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wuapi.h
api_name:
 - UpdateServiceRegistrationState
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# tagUpdateServiceRegistrationState enumeration


## -description


Defines the possible states for an update service.


## -enum-fields




### -field usrsNotRegistered

The service is not registered.


### -field usrsRegistrationPending

The service is pending registration. Registration will be attempted the next time the update agent contacts an update service.


### -field usrsRegistered

The service is registered.

