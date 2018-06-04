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

# _SCESVC_CONFIGURATION_LINE_ structure


## -description


The <b>SCESVC_CONFIGURATION_LINE</b> structure contains information about a line of configuration data. It is used by the 
<a href="https://msdn.microsoft.com/a89ab072-7b7c-4ecd-83fa-26e2689778df">SCESVC_CONFIGURATION_INFO</a> structure.


## -struct-fields




### -field Key

String that contains data key. Typically this is the name of the configuration parameter to which the <b>Value</b> data applies.


### -field Value

String that contains data describing the configuration.


### -field ValueLen

Length of the data stored in <b>Value</b>, in bytes.


## -see-also




<a href="https://msdn.microsoft.com/a89ab072-7b7c-4ecd-83fa-26e2689778df">SCESVC_CONFIGURATION_INFO</a>
 

 

