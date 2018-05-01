---
UID: NF:comsvcs.IGetContextProperties.GetProperty
title: IGetContextProperties::GetProperty method
author: windows-driver-content
description: Retrieves the value of the specified context property.
old-location: cos\igetcontextproperties_getproperty.htm
old-project: cossdk
ms.assetid: 920938a9-44b1-4473-8204-1129b9599a72
ms.author: windowsdriverdev
ms.date: 4/3/2018
ms.keywords: GetProperty method [COM+], GetProperty method [COM+], IGetContextProperties interface, GetProperty,IGetContextProperties.GetProperty, IGetContextProperties, IGetContextProperties interface [COM+], GetProperty method, IGetContextProperties::GetProperty, _cos_IGetContextProperties_GetProperty, comsvcs/IGetContextProperties::GetProperty, cos.igetcontextproperties_getproperty
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: comsvcs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: TRACKING_COLL_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	ComSvcs.h
api_name:
-	IGetContextProperties.GetProperty
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IGetContextProperties::GetProperty method


## -description


Retrieves the value of the specified context property.


## -parameters




### -param name [in]

The name of a current context property.


### -param pProperty [out, retval]

The value(s) of the property.


## -returns



This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.




## -see-also




<a href="https://msdn.microsoft.com/5e960c75-b074-4d4b-b5d6-252c26c70176">IGetContextProperties</a>
 

 

