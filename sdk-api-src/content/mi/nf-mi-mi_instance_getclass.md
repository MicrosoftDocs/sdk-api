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

# MI_Instance_GetClass function


## -description


Gets the <a href="https://msdn.microsoft.com/7f02e0fa-9e58-455d-9cf4-1d1244c44422">MI_Class</a> associated with an 
     instance.


## -parameters




### -param self [in]

A pointer to an instance whose <a href="https://msdn.microsoft.com/7f02e0fa-9e58-455d-9cf4-1d1244c44422">MI_Class</a> structure is 
      to be retrieved.


### -param instanceClass

Returned <a href="https://msdn.microsoft.com/7f02e0fa-9e58-455d-9cf4-1d1244c44422">MI_Class</a>. This 
      <b>MI_Class</b> wraps the 
      <a href="https://msdn.microsoft.com/8e2e2838-5d08-4e51-be96-0928042ccb9f">MI_ClassDecl</a> field inside the 
      <a href="https://msdn.microsoft.com/3dce1817-7995-49e5-8cc0-ee9496665e5c">MI_Instance</a> and does not retrieve anything from the 
      server. This returned class should be deleted via 
      <a href="https://msdn.microsoft.com/a2794f8f-a69a-49f3-8d7e-512c80ea782b">MI_Class_Delete</a>.


## -returns



A value of the <a href="https://msdn.microsoft.com/9AA2B479-E8A5-4F0C-A8A4-06DB7CB7CA2F">MI_Result</a> enumeration that specifies 
      the function return code. This can be one of the following codes.




## -remarks



Different types of classes exist. A dynamic instance has a very flat class declaration with no real 
    qualifiers. Certain 
    <a href="mi_flags.htm">flags</a> in to 
    session objects can also change the type of runtime type information (RTTI) that is returned, such that it has 
    none (types are all strings, flat structure, no qualifiers), basic (types of properties should be correct, but 
    they are flat-structured without qualifiers), standard (best effort at creating hierarchy, but overloaded 
    properties may not show original type in parent class), and full, which is an accurate class declaration. 
    Therefore, how an instance is created or retrieved will depend on the accuracy of the class declaration.




## -see-also




<a href="https://msdn.microsoft.com/7f02e0fa-9e58-455d-9cf4-1d1244c44422">MI_Class</a>



<a href="https://msdn.microsoft.com/8e2e2838-5d08-4e51-be96-0928042ccb9f">MI_ClassDecl</a>



<a href="https://msdn.microsoft.com/a2794f8f-a69a-49f3-8d7e-512c80ea782b">MI_Class_Delete</a>



<a href="https://msdn.microsoft.com/3dce1817-7995-49e5-8cc0-ee9496665e5c">MI_Instance</a>
 

 

