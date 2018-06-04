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

# IUIAutomationElement7::GetCurrentMetadataValue


## -description


Gets metadata from the UI Automation element that indicates how the information should be interpreted. For example, should the string "1/4" be interpreted as a fraction or a date?


## -parameters




### -param targetId [in]

The ID of the property to retrieve.


### -param metadataId [in]

Specifies the type of metadata to retrieve.


### -param returnVal [out, retval]

The metadata.


## -returns



Returns <b>S_OK</b> if successful, otherwise an <b>HRESULT</b> error code.




## -see-also




<a href="winauto.iuiautomationelement7">IUIAutomationElement7</a>



<a href="https://msdn.microsoft.com/70F6AA0E-52CB-49D4-BBAF-2B6367D5E44D">SayAsInterpretAs</a>
 

 

