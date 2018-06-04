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

# _IMAPI_MODE_PAGE_REQUEST_TYPE enumeration


## -description


Defines values that indicate requests sent to a device using the MODE_SENSE10 MMC command.


## -enum-fields




### -field IMAPI_MODE_PAGE_REQUEST_TYPE_CURRENT_VALUES

Requests current settings of the mode page.  This is the most common request type, and the most commonly supported type of this command.


### -field IMAPI_MODE_PAGE_REQUEST_TYPE_CHANGEABLE_VALUES

Requests a mask that indicates settings that are write enabled. A write-enabled setting has a corresponding bit that is set to one in the mask. A read-only setting has a corresponding bit that is set to zero in the mask .


### -field IMAPI_MODE_PAGE_REQUEST_TYPE_DEFAULT_VALUES

Requests the power-on settings of the drive.


### -field IMAPI_MODE_PAGE_REQUEST_TYPE_SAVED_VALUES

Requests a saved configuration for a drive. This functionality might not be supported on all devices.

