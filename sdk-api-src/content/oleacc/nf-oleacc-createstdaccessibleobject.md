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

# CreateStdAccessibleObject function


## -description


Creates an accessible object with the methods and properties of the specified type of system-provided user interface element.


## -parameters




### -param hwnd [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

Window handle of the system-provided user interface element (a control) for which an accessible object is created.


### -param idObject [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LONG</a></b>

Object ID. This value is usually <a href="object_identifiers.htm">OBJID_CLIENT</a>, but it may be another object identifier.


### -param riid

TBD


### -param ppvObject [out]

Type: <b>void**</b>

Address of a pointer variable that receives the address of the specified interface.


#### - riidInterface [in]

Type: <b>REFIID</b>

Reference identifier of the requested interface. This value is one of the following: IID_IAccessible, IID_IDispatch, IID_IEnumVARIANT, or IID_IUnknown.


## -returns



Type: <b>STDAPI</b>

If successful, returns S_OK.

If not successful, returns a standard <a href="https://msdn.microsoft.com/e6deca92-42da-41ab-bfdb-75cbce3022bb">COM error code</a>.




## -remarks



Server applications call this function when they contain a custom UI object that is similar to a system-provided object. Server developers can call <b>CreateStdAccessibleObject</b> to override the <a href="https://msdn.microsoft.com/51e95b01-71e7-435b-85fb-28ee43eb08a7">IAccessible</a> methods and properties as required to match their custom objects. Alternatively, server developers can use Dynamic Annotation to override specific properties without having to use difficult subclassing techniques that <b>CreateStdAccessibleObject</b> requires. Server developers should still use <b>CreateStdAccessibleObject</b> for structural changes, such as hiding a child element or creating a placeholder child element. This approach saves server developers the work of fully implementing all of the <b>IAccessible</b> properties and methods.

This function is similar to <a href="https://msdn.microsoft.com/724b2a38-f7ca-4423-acd4-0871623d1201">CreateStdAccessibleProxy</a>, except that <b>CreateStdAccessibleProxy</b> allows you to specify the class name as a parameter whereas <b>CreateStdAccessibleObject</b> uses the class name associated with the <i>hwnd</i> parameter.




## -see-also




<a href="https://msdn.microsoft.com/724b2a38-f7ca-4423-acd4-0871623d1201">CreateStdAccessibleProxy</a>



<a href="https://msdn.microsoft.com/5a95f002-4fd5-43d3-9b50-7b3f7790300a">IDispatch</a>



<a href="https://msdn.microsoft.com/024e1bfd-8cc2-4839-82ae-bd05dfec6449">Shortcuts for Exposing Custom User Interface Elements</a>
 

 

