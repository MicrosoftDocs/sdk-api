---
UID: NE:wuapi.tagUpdateServiceRegistrationState
title: UpdateServiceRegistrationState (wuapi.h)
description: Defines the possible states for an update service.
helpviewer_keywords: ["UpdateServiceRegistrationState","UpdateServiceRegistrationState enumeration [Windows Update Agent]","usrsNotRegistered","usrsRegistered","usrsRegistrationPending","wua.updateserviceregistrationstate","wuapi/UpdateServiceRegistrationState","wuapi/usrsNotRegistered","wuapi/usrsRegistered","wuapi/usrsRegistrationPending"]
old-location: wua\updateserviceregistrationstate.htm
tech.root: wua
ms.assetid: 798d1392-a8dc-4063-b33d-159a507161f1
ms.date: 12/05/2018
ms.keywords: UpdateServiceRegistrationState, UpdateServiceRegistrationState enumeration [Windows Update Agent], usrsNotRegistered, usrsRegistered, usrsRegistrationPending, wua.updateserviceregistrationstate, wuapi/UpdateServiceRegistrationState, wuapi/usrsNotRegistered, wuapi/usrsRegistered, wuapi/usrsRegistrationPending
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: UpdateServiceRegistrationState
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagUpdateServiceRegistrationState
 - wuapi/tagUpdateServiceRegistrationState
 - UpdateServiceRegistrationState
 - wuapi/UpdateServiceRegistrationState
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wuapi.h
api_name:
 - UpdateServiceRegistrationState
---

# UpdateServiceRegistrationState enumeration


## -description

Defines the possible states for an update service.

## -enum-fields

### -field usrsNotRegistered:1

The service is not registered.

### -field usrsRegistrationPending:2

The service is pending registration. Registration will be attempted the next time the update agent contacts an update service.

### -field usrsRegistered:3

The service is registered.

