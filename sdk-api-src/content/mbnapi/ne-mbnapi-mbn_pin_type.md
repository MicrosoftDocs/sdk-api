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

# MBN_PIN_TYPE enumeration


## -description


The <b>MBN_PIN_TYPE</b> enumerated type indicates the type of password required for unlocking the information stored on the interface.


## -enum-fields




### -field MBN_PIN_TYPE_NONE

Indicates that no PIN is pending to be entered.


### -field MBN_PIN_TYPE_CUSTOM

Indicates a custom PIN code.


### -field MBN_PIN_TYPE_PIN1

Indicates a PIN1 code.  For CDMA devices, PIN1 represents the power-on device lock code.  For GSM devices, PIN1 represents the SIM lock, also referred to  as PIN in GSM terminology.


### -field MBN_PIN_TYPE_PIN2

Indicates a PIN2 code.


### -field MBN_PIN_TYPE_DEVICE_SIM_PIN

Indicates a device to SIM password.


### -field MBN_PIN_TYPE_DEVICE_FIRST_SIM_PIN

Indicates a device to very first SIM password.


### -field MBN_PIN_TYPE_NETWORK_PIN

Indicates a network personalization password.


### -field MBN_PIN_TYPE_NETWORK_SUBSET_PIN

Indicates a network subset personalization password.


### -field MBN_PIN_TYPE_SVC_PROVIDER_PIN

Indicates a Service Provider (SP) personalization password.


### -field MBN_PIN_TYPE_CORPORATE_PIN

Indicates a corporate personalization password.


### -field MBN_PIN_TYPE_SUBSIDY_LOCK

Indicates a subsidy unlock code.

