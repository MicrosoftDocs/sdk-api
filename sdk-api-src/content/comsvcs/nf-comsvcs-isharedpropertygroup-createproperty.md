---
UID: NF:comsvcs.ISharedPropertyGroup.CreateProperty
title: ISharedPropertyGroup::CreateProperty
author: windows-sdk-content
description: Creates a new shared property with the specified name.
old-location: cos\isharedpropertygroup_createproperty.htm
tech.root: cossdk
ms.assetid: bc34ec47-b39f-49fd-a8dd-8c96bb708e88
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: CreateProperty, CreateProperty method [COM+], CreateProperty method [COM+],ISharedPropertyGroup interface, ISharedPropertyGroup interface [COM+],CreateProperty method, ISharedPropertyGroup.CreateProperty, ISharedPropertyGroup::CreateProperty, _cos_ISharedPropertyGroup_CreateProperty, comsvcs/ISharedPropertyGroup::CreateProperty, cos.isharedpropertygroup_createproperty
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
 - ISharedPropertyGroup.CreateProperty
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISharedPropertyGroup::CreateProperty


## -description


Creates a new shared property with the specified name. If a shared property by that name already exists, <b>CreateProperty</b> returns a reference to the existing property. 



## -parameters




### -param Name [in]

The name of the property to create. You can use this name later to obtain a reference to this property by using the <a href="https://msdn.microsoft.com/ffbd82a8-35d5-4c9b-bf03-91f48dddc189">get_Property</a> method.


### -param fExists [out]

A reference to a Boolean value that is set to VARIANT_TRUE on return from this method if the shared property specified in the <i>Name</i> parameter existed prior to this call, and VARIANT_FALSE if the property was created by this call.


### -param ppProp [out]

A reference to a <a href="https://msdn.microsoft.com/19ed8d50-3ac1-408e-9f25-09f284d025f1">SharedProperty</a> object with the name specified in the <i>Name</i> parameter, or <b>NULL</b> if an error is encountered.


## -returns



This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.




## -remarks



When you create a shared property, its value is set to the default, which is a VT_I4 VARIANT with a value of 0.



If you create a shared property with the <b>CreateProperty</b> method, you can access that property only by using the <a href="https://msdn.microsoft.com/ffbd82a8-35d5-4c9b-bf03-91f48dddc189">get_Property</a> method. You cannot assign a numeric index to the same property and then access it by using the <a href="https://msdn.microsoft.com/186cbf9f-a01b-4331-9f18-645d9e47f106">get_PropertyByPosition</a> method.



The same shared property group can contain some <a href="https://msdn.microsoft.com/19ed8d50-3ac1-408e-9f25-09f284d025f1">SharedProperty</a> objects that are identified by name and others that are identified by position.




## -see-also




<a href="https://msdn.microsoft.com/d3c3e888-fe08-4ea6-b94c-fdfcbe7fd08a">ISharedProperty</a>



<a href="https://msdn.microsoft.com/e7f23c83-40d3-4b08-a185-cd6e3260e0a9">ISharedPropertyGroup</a>
 

 

