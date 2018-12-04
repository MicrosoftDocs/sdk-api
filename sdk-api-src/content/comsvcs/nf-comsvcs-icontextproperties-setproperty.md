---
UID: NF:comsvcs.IContextProperties.SetProperty
title: IContextProperties::SetProperty
author: windows-sdk-content
description: Sets a context object property.
old-location: cos\icontextproperties_setproperty.htm
tech.root: cossdk
ms.assetid: 4f6a27a2-37e9-4d4b-9d7e-916d791f03a5
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: IContextProperties interface [COM+],SetProperty method, IContextProperties.SetProperty, IContextProperties::SetProperty, SetProperty, SetProperty method [COM+], SetProperty method [COM+],IContextProperties interface, _cos_IContextProperties_SetProperty, comsvcs/IContextProperties::SetProperty, cos.icontextproperties_setproperty
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ComSvcs.h
api_name:
 - IContextProperties.SetProperty
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IContextProperties::SetProperty


## -description


Sets a context object property.


## -parameters




### -param name [in]

The name of the context object property to be set. See <a href="https://msdn.microsoft.com/dc7748b4-5cf4-41c6-af7d-82b2478b084c">GetProperty</a> for a list of valid property names.


### -param property [in]

The context object property value.


## -returns



This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.




## -see-also




<a href="https://msdn.microsoft.com/95a5cfda-7587-496e-ba16-0dd2e8a4db32">IContextProperties</a>
 

 

