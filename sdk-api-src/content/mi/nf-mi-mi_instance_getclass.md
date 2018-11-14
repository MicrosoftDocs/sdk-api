---
UID: NF:mi.MI_Instance_GetClass
title: MI_Instance_GetClass function
author: windows-sdk-content
description: Gets the MI_Class associated with an instance.
old-location: wmi_v2\mi_instance_getclass.htm
tech.root: WMI_v2
ms.assetid: 4799e9f0-f233-499f-acec-9041074eab42
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: MI_Instance_GetClass, MI_Instance_GetClass function [Windows Management Infrastructure (MI)], mi/MI_Instance_GetClass, wmi_v2.mi_instance_getclass
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: mi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8
req.target-min-winversvr: Windows Server 2012
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
 - HeaderDef
api_location:
 - Mi.h
api_name:
 - MI_Instance_GetClass
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Management Framework 3.0 on Windows Server 2008 R2 with SP1,     Windows 7 with SP1, and Windows Server 2008 with SP2
- apiref
: 
- 
: 
- MI_Instance_GetClass
: 
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
    <a href="https://msdn.microsoft.com/en-us/library/JJ653875(v=VS.85).aspx">flags</a> in to 
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
 

 

