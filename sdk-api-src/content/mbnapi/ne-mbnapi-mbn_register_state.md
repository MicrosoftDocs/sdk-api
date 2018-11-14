---
UID: NE:mbnapi.MBN_REGISTER_STATE
title: MBN_REGISTER_STATE
author: windows-sdk-content
description: The MBN_REGISTER_STATE enumerated type indicates the network registration state of a Mobile Broadband device.
old-location: mbn\mbn_register_state.htm
tech.root: mbn
ms.assetid: cbe29357-b374-4764-9322-6308b98ddc3e
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: MBN_REGISTER_STATE, MBN_REGISTER_STATE enumeration [Microsoft Broadband Networks], MBN_REGISTER_STATE_DENIED, MBN_REGISTER_STATE_DEREGISTERED, MBN_REGISTER_STATE_HOME, MBN_REGISTER_STATE_NONE, MBN_REGISTER_STATE_PARTNER, MBN_REGISTER_STATE_ROAMING, MBN_REGISTER_STATE_SEARCHING, mbn.mbn_register_state, mbnapi/MBN_REGISTER_STATE, mbnapi/MBN_REGISTER_STATE_DENIED, mbnapi/MBN_REGISTER_STATE_DEREGISTERED, mbnapi/MBN_REGISTER_STATE_HOME, mbnapi/MBN_REGISTER_STATE_NONE, mbnapi/MBN_REGISTER_STATE_PARTNER, mbnapi/MBN_REGISTER_STATE_ROAMING, mbnapi/MBN_REGISTER_STATE_SEARCHING
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: mbnapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Mbnapi.idl
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
 - mbnapi.h
api_name:
 - MBN_REGISTER_STATE
product: Windows
targetos: Windows
req.typenames: MBN_REGISTER_STATE
req.redist: 
---

# MBN_REGISTER_STATE enumeration


## -description


The <b>MBN_REGISTER_STATE</b> enumerated type indicates the network registration state of a Mobile Broadband device.


## -enum-fields




### -field MBN_REGISTER_STATE_NONE

The device registration state is unknown.  This state may be set upon failure of registration mode change requests.


### -field MBN_REGISTER_STATE_DEREGISTERED

The device is not registered and not searching for a provider.


### -field MBN_REGISTER_STATE_SEARCHING

The device is not registered and is searching for a provider.


### -field MBN_REGISTER_STATE_HOME

The device is on a home provider.


### -field MBN_REGISTER_STATE_ROAMING

The device is on a roaming provider.


### -field MBN_REGISTER_STATE_PARTNER

The device is on a roaming partner.


### -field MBN_REGISTER_STATE_DENIED

The device was denied registration.  Emergency voice calls may be made.  This applies to voice and not data.

