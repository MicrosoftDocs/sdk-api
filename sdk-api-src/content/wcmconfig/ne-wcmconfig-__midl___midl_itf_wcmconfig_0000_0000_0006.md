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

# __MIDL___MIDL_itf_wcmconfig_0000_0000_0006 enumeration


## -description


Describes the status of the user.


## -enum-fields




### -field UnknownStatus

Indicates a problem with the store.


### -field UserRegistered

Indicates that the store is registered, but is not currently loaded for use.


### -field UserUnregistered

Indicates that the store does not currently exist.


### -field UserLoaded

Indicates that the store is registered, loaded, and ready for use.


### -field UserUnloaded

This has the same semantics as <b>UserRegistered</b>.


## -remarks



<b>UserUnloaded</b>, <b>UserUnregistered</b>, and <b>UnknownStatus</b> should not appear in typical use.



