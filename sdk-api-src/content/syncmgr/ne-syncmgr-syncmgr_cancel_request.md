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

# SYNCMGR_CANCEL_REQUEST enumeration


## -description


Describes a request by the user to cancel a synchronization.


## -enum-fields




### -field SYNCMGR_CR_NONE

No cancelation request has been made.


### -field SYNCMGR_CR_CANCEL_ITEM

Stop the synchronization of the current item, but continue the synchronization of other items.


### -field SYNCMGR_CR_CANCEL_ALL

Stop the synchronization entirely.


### -field SYNCMGR_CR_MAX

The maximum valid <a href="https://msdn.microsoft.com/81cf8dcc-c847-41e0-82e2-b5f547fc03cf">SYNCMGR_CANCEL_REQUEST</a> value.

