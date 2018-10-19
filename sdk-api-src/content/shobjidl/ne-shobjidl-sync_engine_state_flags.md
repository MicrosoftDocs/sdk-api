---
UID: NE:shobjidl.SYNC_ENGINE_STATE_FLAGS
title: SYNC_ENGINE_STATE_FLAGS
author: windows-sdk-content
description: Specifies values used by any sync engine to expose their internal engine states to the Property Store's PKEY_StorageProviderStatus value in the File Indexer To update the property, first call IShellItem2::GetPropertyStore with the GPS_EXTRINSICPROPERTIES flag. Next, call the IPropertyStore::SetValue method of the returned object, specifying the PKEY_StorageProviderStatus key, to set the property's bitmask value using these SYNC_ENGINE_STATE_FLAGS.
old-location: properties\SYNC_ENGINE_STATE_FLAGS.htm
tech.root: properties
ms.assetid: BD81EE89-AAB3-4270-8F62-B26708740EE1
ms.author: windowssdkdev
ms.date: 10/18/2018
ms.keywords: PLACEHOLDER_STATES, PLACEHOLDER_STATES enumeration [Windows Properties], SESF_ALL_FLAGS, SESF_AUTHENTICATION_ERROR, SESF_NONE, SESF_PAUSED_DUE_TO_CLIENT_POLICY, SESF_PAUSED_DUE_TO_DISK_SPACE_FULL, SESF_PAUSED_DUE_TO_METERED_NETWORK, SESF_PAUSED_DUE_TO_SERVICE_POLICY, SESF_SERVICE_QUOTA_EXCEEDED_LIMIT, SESF_SERVICE_QUOTA_NEARING_LIMIT, SESF_SERVICE_UNAVAILABLE, SYNC_ENGINE_STATE_FLAGS, properties.SYNC_ENGINE_STATE_FLAGS, shobjidl/PLACEHOLDER_STATES, shobjidl/SESF_ALL_FLAGS, shobjidl/SESF_AUTHENTICATION_ERROR, shobjidl/SESF_NONE, shobjidl/SESF_PAUSED_DUE_TO_CLIENT_POLICY, shobjidl/SESF_PAUSED_DUE_TO_DISK_SPACE_FULL, shobjidl/SESF_PAUSED_DUE_TO_METERED_NETWORK, shobjidl/SESF_PAUSED_DUE_TO_SERVICE_POLICY, shobjidl/SESF_SERVICE_QUOTA_EXCEEDED_LIMIT, shobjidl/SESF_SERVICE_QUOTA_NEARING_LIMIT, shobjidl/SESF_SERVICE_UNAVAILABLE
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: shobjidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
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
 - Shobjidl.h
api_name:
 - SYNC_ENGINE_STATE_FLAGS
product: Windows
targetos: Windows
req.typenames: SYNC_ENGINE_STATE_FLAGS
req.redist: 
---

# SYNC_ENGINE_STATE_FLAGS enumeration


## -description


Specifies values used by any sync engine to expose their internal engine states to the Property Store's PKEY_StorageProviderStatus value in the File Indexer 

            

To update the property, first call <a href="https://msdn.microsoft.com/706b2551-a9b0-4368-babb-e54cea6d297e">IShellItem2::GetPropertyStore</a> with the <a href="https://msdn.microsoft.com/d3fde1b9-b19f-431d-9cea-bffc289ee683">GPS_EXTRINSICPROPERTIES</a> flag. Next, call the <a href="https://msdn.microsoft.com/f5ede696-0cd4-41e2-9576-822e3f9909e7">IPropertyStore::SetValue</a> method of the returned object, specifying the PKEY_StorageProviderStatus key, to set the property's bitmask value using these SYNC_ENGINE_STATE_FLAGS.


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

