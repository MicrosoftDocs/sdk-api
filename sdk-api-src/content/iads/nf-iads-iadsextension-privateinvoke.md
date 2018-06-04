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

# IADsExtension::PrivateInvoke


## -description


The <b>IADsExtension::PrivateInvoke</b> method is normally called by ADSI after the  <a href="https://msdn.microsoft.com/533faef7-d504-443c-83e7-7eaf461ce550">IADsExtension::PrivateGetIDsOfNames</a> method. This method can either have a custom implementation or it can delegate the operation to <a href="69b89e5c-2a04-4a6a-beb0-18e68f8866ac">IDispatch::DispInvoke</a> method.


## -parameters




### -param dispidMember [in]

Identifies the member. Use the <a href="https://msdn.microsoft.com/533faef7-d504-443c-83e7-7eaf461ce550">IADsExtension::PrivateGetIDsOfNames</a> method to obtain the dispatch identifier.


### -param riid [in]

Reserved for future use. Must be IID_NULL.


### -param lcid [in]

The locale context in which to interpret arguments. The <a href="https://msdn.microsoft.com/533faef7-d504-443c-83e7-7eaf461ce550">IADsExtension::PrivateGetIDsOfNames</a> function uses <i>lcid</i>. It is also passed to the <b>PrivateInvoke</b> method to allow the object to interpret the arguments that are specific to a locale.


### -param wFlags [in]

Flags that describe the context of the <b>PrivateInvoke</b> call, include.



#### DISPATCH_METHOD

The member is invoked as a method. If a property has the same name, both this and the <b>DISPATCH_PROPERTYGET</b> flag may be set.



#### DISPATCH_PROPERTYGET

The member is retrieved as a property or data member.



#### DISPATCH_PROPERTYPUT

The member is changed as a property or data member.



#### DISPATCH_PROPERTYPUTREF

The member is changed by a reference assignment, rather than a value assignment. This flag is valid only when the property accepts a reference to an object.


### -param pdispparams [in]

Pointer to a <a href="a16e5a21-766e-4287-b039-13429aa78f8b">DISPPARAMS</a> structure that receives an array of arguments, an array of argument DISPIDs for named arguments, and counts for the number of elements in the arrays.


### -param pvarResult [out]

Pointer to the location where the result is to be stored, or <b>NULL</b> if the caller expects no result. This argument is ignored if <b>DISPATCH_PROPERTYPUT</b> or <b>DISPATCH_PROPERTYPUTREF</b> is specified.


### -param pexcepinfo [out]

Pointer to a structure that contains exception data. This structure should be filled in if <b>DISP_E_EXCEPTION</b> is returned. Can be <b>NULL</b>.


### -param puArgErr [out]

The index within the <b>rgvarg</b> member of the <a href="a16e5a21-766e-4287-b039-13429aa78f8b">DISPPARAMS</a> structure in <i>pdispparams</i> for the first argument that has an error. Arguments are stored in the <b>rgvarg</b> array in reverse order, so the first argument is the one with the highest index in the array. This parameter is returned only when the resulting return value is <b>DISP_E_TYPEMISMATCH</b> or <b>DISP_E_PARAMNOTFOUND</b>.


## -returns



This method supports the standard return values, as well as the following.

For more information about other return values, see  <a href="https://msdn.microsoft.com/573889e4-37af-4aca-afd7-ef06bcf8aa0d">ADSI Error Codes</a>.




## -see-also




<a href="https://msdn.microsoft.com/573889e4-37af-4aca-afd7-ef06bcf8aa0d">ADSI Error Codes</a>



<a href="69b89e5c-2a04-4a6a-beb0-18e68f8866ac">DispInvoke</a>



<a href="https://msdn.microsoft.com/05681526-2232-4341-859d-6773f7a58431">IADsExtension</a>



<a href="https://msdn.microsoft.com/533faef7-d504-443c-83e7-7eaf461ce550">IADsExtension::PrivateGetIDsOfNames</a>
 

 

