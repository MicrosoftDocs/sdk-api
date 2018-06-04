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

# IFhTarget::GetStringProperty


## -description


Retrieves a string property of the File History backup target that is represented by an <a href="https://msdn.microsoft.com/5A73A81A-72A3-4794-86E5-9CA8FCA200C0">IFhTarget</a> interface.


## -parameters




### -param PropertyType [in]

Specifies the string property. See the <a href="https://msdn.microsoft.com/0A39626B-942F-4BD6-930D-15E9D401F0FF">FH_TARGET_PROPERTY_TYPE</a> enumeration for the list of possible string property types.


### -param PropertyValue [out]

This parameter must be <b>NULL</b> on input. On output, it receives a pointer to a string that contains the string property. This string is allocated by calling <a href="https://msdn.microsoft.com/9e0437a2-9b4a-4576-88b0-5cb9d08ca29b">SysAllocString</a>. You must call <a href="https://msdn.microsoft.com/8f230ee3-5f6e-4cb9-a910-9c90b754dcd3">SysFreeString</a> to free the string when it is no longer needed.


## -returns



If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code such as one of the values defined in the FhErrors.h header file.




## -remarks



The <a href="https://msdn.microsoft.com/0A39626B-942F-4BD6-930D-15E9D401F0FF">FH_TARGET_PROPERTY_TYPE</a> enumeration defines property types for string properties and numeric properties. However, the <b>IFhTarget::GetStringProperty</b> method can only be used to retrieve string properties. Numeric properties must be retrieved by calling the <a href="https://msdn.microsoft.com/3FA2F3AB-A406-4F19-AA5A-0D5596F1BF2C">IFhTarget::GetNumericalProperty</a> method.




## -see-also




<a href="https://msdn.microsoft.com/0A39626B-942F-4BD6-930D-15E9D401F0FF">FH_TARGET_PROPERTY_TYPE</a>



<a href="https://msdn.microsoft.com/5A73A81A-72A3-4794-86E5-9CA8FCA200C0">IFhTarget</a>



<a href="https://msdn.microsoft.com/3FA2F3AB-A406-4F19-AA5A-0D5596F1BF2C">IFhTarget::GetNumericalProperty</a>
 

 

