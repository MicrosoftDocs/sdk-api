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

# IVisualTreeService::CreateInstance


## -description


Creates an instance of any XAML runtime, enum, or primitive type.


## -parameters




### -param typeName [in]

The type name. (Should be from <a href="https://msdn.microsoft.com/111D10AB-2C16-4D21-A716-968C810B928F">PropertyChainValue.Type</a>.)


### -param value [in]

The value to set on a primitive or enum type. <b>null</b> if creating a XAML runtime type.


### -param pInstanceHandle [out, retval]

An instance handle to newly created instance.


## -returns



If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -remarks



 For primitives and enums, <i>value</i> should be 
    set to desired value. For XAML runtime types, <i>value</i> should be <b>null</b>.




## -see-also




<a href="https://msdn.microsoft.com/5C0896E4-E37E-49DF-B303-1814BCA6F5B3">IVisualTreeService</a>
 

 

