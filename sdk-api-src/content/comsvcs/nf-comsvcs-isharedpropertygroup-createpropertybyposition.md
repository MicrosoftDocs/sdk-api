---
UID: NF:comsvcs.ISharedPropertyGroup.CreatePropertyByPosition
title: ISharedPropertyGroup::CreatePropertyByPosition
author: windows-sdk-content
description: Creates a new shared property with the specified index.
old-location: cos\isharedpropertygroup_createpropertybyposition.htm
old-project: cossdk
ms.assetid: 47e0e230-0952-4afb-a757-af387a7cddfb
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: CreatePropertyByPosition, CreatePropertyByPosition method [COM+], CreatePropertyByPosition method [COM+],ISharedPropertyGroup interface, ISharedPropertyGroup interface [COM+],CreatePropertyByPosition method, ISharedPropertyGroup.CreatePropertyByPosition, ISharedPropertyGroup::CreatePropertyByPosition, _cos_ISharedPropertyGroup_CreatePropertyByPosition, comsvcs/ISharedPropertyGroup::CreatePropertyByPosition, cos.isharedpropertygroup_createpropertybyposition
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: TRACKING_COLL_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ComSvcs.h
api_name:
 - ISharedPropertyGroup.CreatePropertyByPosition
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ISharedPropertyGroup::CreatePropertyByPosition


## -description


Creates a new shared property with the specified index. If a shared property with the specified index already exists, <b>CreatePropertyByPosition</b> returns a reference to the existing one. 



## -parameters




### -param Index [in]

The numeric index within the <a href="https://msdn.microsoft.com/20fd32f0-b2b2-4bed-8c59-1d1fdc8a399e">SharedPropertyGroup</a> object by which the new property is referenced. You can use this index later to retrieve the shared property with the <a href="https://msdn.microsoft.com/186cbf9f-a01b-4331-9f18-645d9e47f106">get_PropertyByPosition</a> method.


### -param fExists [out]

A reference to a Boolean value. If <i>fExists</i> is set to VARIANT_TRUE on return from this method, the shared property specified by <i>Index</i> existed prior to this call. If it is set to VARIANT_FALSE, the property was created by this call.


### -param ppProp [out]

A reference to a shared property object identified by the numeric index passed in the <i>Index</i> parameter, or <b>NULL</b> if an error is encountered.


## -returns



This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.




## -remarks



When you create a shared property, its value is set to the default, which is a VT_I4 VARIANT with a value of 0.



If you create a <a href="https://msdn.microsoft.com/19ed8d50-3ac1-408e-9f25-09f284d025f1">SharedProperty</a> object with the <b>CreatePropertyByPosition</b> method, you can access that property only by using the <a href="https://msdn.microsoft.com/186cbf9f-a01b-4331-9f18-645d9e47f106">get_PropertyByPosition</a> method. You cannot assign a string name to the same property and then access it by using the <a href="https://msdn.microsoft.com/ffbd82a8-35d5-4c9b-bf03-91f48dddc189">get_Property</a> method. Accessing a property by position is faster than accessing a property by using a string name because it requires less overhead.

The same shared property group can contain some <a href="https://msdn.microsoft.com/19ed8d50-3ac1-408e-9f25-09f284d025f1">SharedProperty</a> objects that are identified by position and others that are identified by name.




## -see-also




<a href="https://msdn.microsoft.com/d3c3e888-fe08-4ea6-b94c-fdfcbe7fd08a">ISharedProperty</a>



<a href="https://msdn.microsoft.com/e7f23c83-40d3-4b08-a185-cd6e3260e0a9">ISharedPropertyGroup</a>
 

 

