---
UID: NE:syncregistration.__MIDL___MIDL_itf_syncregistration_0000_0007_0001
title: "__MIDL___MIDL_itf_syncregistration_0000_0007_0001"
author: windows-sdk-content
description: Represents the different types of synchronization registration events.
old-location: winsync\sync_registration_event.htm
tech.root: winsync
ms.assetid: c8fb3de0-0f2e-4926-b37f-3043fcc2efb3
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: SRE_CONFIGUI_ADDED, SRE_CONFIGUI_REMOVED, SRE_CONFIGUI_UPDATED, SRE_PROVIDER_ADDED, SRE_PROVIDER_REMOVED, SRE_PROVIDER_STATE_CHANGED, SRE_PROVIDER_UPDATED, SYNC_REGISTRATION_EVENT, SYNC_REGISTRATION_EVENT enumeration [Windows Sync], __MIDL___MIDL_itf_syncregistration_0000_0007_0001, syncregistration/SRE_CONFIGUI_ADDED, syncregistration/SRE_CONFIGUI_REMOVED, syncregistration/SRE_CONFIGUI_UPDATED, syncregistration/SRE_PROVIDER_ADDED, syncregistration/SRE_PROVIDER_REMOVED, syncregistration/SRE_PROVIDER_STATE_CHANGED, syncregistration/SRE_PROVIDER_UPDATED, syncregistration/SYNC_REGISTRATION_EVENT, winsync.sync_registration_event
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: syncregistration.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - Syncregistration.h
api_name:
 - SYNC_REGISTRATION_EVENT
product: Windows
targetos: Windows
req.typenames: SYNC_REGISTRATION_EVENT
req.redist: 
---

# __MIDL___MIDL_itf_syncregistration_0000_0007_0001 enumeration


## -description


Represents the different types of synchronization registration events.


## -enum-fields




### -field SRE_PROVIDER_ADDED

A synchronization provider registration has been added.


### -field SRE_PROVIDER_REMOVED

A synchronization provider registration has been removed.


### -field SRE_PROVIDER_UPDATED

The property store (represented by the <b>IPropertyStore</b> interface) of a synchronization provider or a synchronization provider configuration UI has changed.


### -field SRE_PROVIDER_STATE_CHANGED

The synchronization provider state has changed.


### -field SRE_CONFIGUI_ADDED

A synchronization provider configuration UI has been added.


### -field SRE_CONFIGUI_REMOVED

A synchronization provider configuration UI has been removed.


### -field SRE_CONFIGUI_UPDATED

A synchronization provider configuration UI has been updated.


## -see-also




<a href="https://msdn.microsoft.com/efd6d871-8c1a-4653-b8a5-9e2d8872c499">Windows Sync Registration Enumerations</a>
 

 

