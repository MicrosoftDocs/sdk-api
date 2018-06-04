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

# SYNC_ENGINE_STATE_FLAGS enumeration


## -description


Specifies values used by any sync engine to expose their internal engine states to the Property Store's PKEY_StorageProviderStatus value in the File Indexer 

            

To update the property, first call <a href="https://msdn.microsoft.com/706b2551-a9b0-4368-babb-e54cea6d297e">IShellItem2::GetPropertyStore</a> with the <a href="https://msdn.microsoft.com/d3fde1b9-b19f-431d-9cea-bffc289ee683">GPS_EXTRINSICPROPERTIES</a> flag. Next, call the <a href="https://msdn.microsoft.com/library/windows/hardware/ff536963">IPropertyStore::SetValue</a> method of the returned object, specifying the PKEY_StorageProviderStatus key, to set the property's bitmask value using these SYNC_ENGINE_STATE_FLAGS.


## -enum-fields




### -field SESF_NONE

No state.


### -field SESF_SERVICE_QUOTA_NEARING_LIMIT

The user's cloud storage quota is nearing capacity. This is dependent on the user's total quota space.


### -field SESF_SERVICE_QUOTA_EXCEEDED_LIMIT

The user's cloud storage quota is filled.


### -field SESF_AUTHENTICATION_ERROR

The user's account credentials are invalid.


### -field SESF_PAUSED_DUE_TO_METERED_NETWORK

The sync engine is paused because of metered network settings.


### -field SESF_PAUSED_DUE_TO_DISK_SPACE_FULL

The drive that contains the sync engine's content has reached the maximum allowed space.


### -field SESF_PAUSED_DUE_TO_CLIENT_POLICY

The user has exceeded their daily limit of requests or data transfers to the service.


### -field SESF_PAUSED_DUE_TO_SERVICE_POLICY

The service has requested the system to throttle requests.


### -field SESF_SERVICE_UNAVAILABLE

The service can't be reached at this time.


### -field SESF_PAUSED_DUE_TO_USER_REQUEST


### -field SESF_ALL_FLAGS

A bitmask value for all valid SYNC_ENGINE_STATE_FLAGS flags.

