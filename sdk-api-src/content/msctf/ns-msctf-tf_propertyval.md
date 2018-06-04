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

# TF_PROPERTYVAL structure


## -description



The <b>TF_PROPERTYVAL</b> structure contains property value data. This structure is used with the <a href="https://msdn.microsoft.com/b0fe154c-df33-443d-95a2-f41e7b02def8">IEnumTfPropertyValue::Next</a> method.




## -struct-fields




### -field guidId

A <b>GUID</b> that identifies the property type. This can be a custom identifier or one of the <a href="https://msdn.microsoft.com/d88f2eba-4c98-4b32-96e1-cd019fe0f7ad">predefined property identifiers</a>.


### -field varValue

A <b>VARIANT</b> that contains the value of the property specified by <b>guidId</b>. The user must know the type and format of this data.


## -see-also




<a href="https://msdn.microsoft.com/b0fe154c-df33-443d-95a2-f41e7b02def8">IEnumTfPropertyValue::Next
      </a>



<a href="https://msdn.microsoft.com/d88f2eba-4c98-4b32-96e1-cd019fe0f7ad">
        Predefined Properties
      </a>
 

 

