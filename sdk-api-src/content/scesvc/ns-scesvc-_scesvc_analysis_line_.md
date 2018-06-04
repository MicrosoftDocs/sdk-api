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

# _SCESVC_ANALYSIS_LINE_ structure


## -description


The <b>SCESVC_ANALYSIS_LINE</b> structure contains the key, value, and value length for a specific line specified by an 
<a href="https://msdn.microsoft.com/4f0273df-435d-4324-b8ce-a774da935059">SCESVC_ANALYSIS_INFO</a> structure.


## -struct-fields




### -field Key

String that contains data key. Typically, this is the name of the configuration parameter to which the <b>Value</b> data applies.


### -field Value

Data describing the analysis result for the key. This can be binary data.


### -field ValueLen

Length of the data stored in <b>Value</b>, in bytes.


## -see-also




<a href="https://msdn.microsoft.com/4f0273df-435d-4324-b8ce-a774da935059">SCESVC_ANALYSIS_INFO</a>
 

 

