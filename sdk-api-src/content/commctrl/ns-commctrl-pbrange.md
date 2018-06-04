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

# PBRANGE structure


## -description


Contains information about the high and low limits of a progress bar control. This structure is used with the <a href="https://msdn.microsoft.com/676b7a37-bdde-4307-9888-9a0cf40db2db">PBM_GETRANGE</a> message. 


## -struct-fields




### -field iLow

Type: <b>int</b>

Low limit for the progress bar control. This is a signed integer. 


### -field iHigh

Type: <b>int</b>

High limit for the progress bar control. This is a signed integer. 

