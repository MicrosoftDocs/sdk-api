---
UID: NS:mi._MI_ClassFT
title: MI_ClassFT (mi.h)
author: windows-sdk-content
description: A support structure used in the MI_Class structure. Use the functions with the name prefix &#0034;MI_Class_&#0034; to manipulate these structures.
old-location: wmi_v2\mi_classft.htm
tech.root: wmi_v2
ms.assetid: 464dd009-5d99-483c-9e94-82ab07290189
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: MI_ClassFT, MI_ClassFT structure [Windows Management Infrastructure (MI)], mi/MI_ClassFT, wmi_v2.mi_classft
ms.topic: struct
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
 - MI_ClassFT
product: Windows
targetos: Windows
req.typenames: MI_ClassFT
req.redist: Windows Management Framework 3.0 on Windows Server 2008 R2 with SP1,     Windows 7 with SP1, and Windows Server 2008 with SP2
---

# MI_ClassFT structure


## -description


A support structure used in the <a href="https://msdn.microsoft.com/7f02e0fa-9e58-455d-9cf4-1d1244c44422">MI_Class</a> structure. 
     Use the functions with the name prefix "MI_Class_" to manipulate these structures.


## -struct-fields




### -field MI_Result

TBD 




#### - Clone

Clones an <a href="https://msdn.microsoft.com/7f02e0fa-9e58-455d-9cf4-1d1244c44422">MI_Class</a> object. See 
       <a href="https://msdn.microsoft.com/a95b867c-7567-4ea4-a02c-049002de2109">MI_Class_Clone</a>.


#### - Delete

Delete an <a href="https://msdn.microsoft.com/7f02e0fa-9e58-455d-9cf4-1d1244c44422">MI_Class</a> object. See 
       <a href="https://msdn.microsoft.com/a2794f8f-a69a-49f3-8d7e-512c80ea782b">MI_Class_Delete</a>.


#### - GetClassName

Retrieves the class name of the class. See 
       <a href="https://msdn.microsoft.com/405639e7-74b0-4cda-9883-f8442976200a">MI_Class_GetClassName</a>.


#### - GetClassQualifierSet

Retrieve an object from a class that allows the class qualifiers to be queried. See 
       <a href="https://msdn.microsoft.com/900ae879-a728-43a9-8dcb-de20a50f8dce">MI_Class_GetClassQualifierSet</a>.


#### - GetElement

Retrieves information about a named class element. See 
       <a href="https://msdn.microsoft.com/eb13ea2b-eac6-4df2-8088-eb47449838b8">MI_Class_GetElement</a>.


#### - GetElementAt

Retrieves information about a specific class element given the element index (Indexes start from 0). See 
       <a href="https://msdn.microsoft.com/f5479cc7-e3f6-447f-a8f8-dc08f3babe54">MI_Class_GetElementAt</a>.


#### - GetElementCount

Retrieves the number of elements in a class. See 
       <a href="https://msdn.microsoft.com/f6db81ca-0411-4693-8bcc-830d4fd757ca">MI_Class_GetElementCount</a> .


#### - GetMethod

Get method information based on a method name. See 
       <a href="https://msdn.microsoft.com/9e6f6ef0-ca19-4416-baf7-bb2ab1d6d33d">MI_Class_GetMethod</a>.


#### - GetMethodAt

Get method information based on a method index. See 
       <a href="https://msdn.microsoft.com/00239417-f771-48fa-afce-fef2ec99a171">MI_Class_GetMethodAt</a>.


#### - GetMethodCount

Retrieves the number of class methods. See 
       <a href="https://msdn.microsoft.com/7190273e-bed5-4888-87c6-7e2d44aae703">MI_Class_GetMethodCount</a>.


#### - GetNameSpace

Retrieves the namespace of the class. See 
       <a href="https://msdn.microsoft.com/64ee42d6-d6ad-4a41-83f4-48de191a853c">MI_Class_GetNameSpace</a>.


#### - GetParentClass

Get the parent class for the specified class. See 
       <a href="https://msdn.microsoft.com/e90e3072-7d01-4959-bfee-c85ea89775a2">MI_Class_GetParentClass</a>.


#### - GetParentClassName

Get the parent class name of the class. See 
       <a href="https://msdn.microsoft.com/a7e183f1-1136-46e0-a53d-39d06767e380">MI_Class_GetParentClassName</a>.


#### - GetServerName

Retrieves the server name of the class. See 
       <a href="https://msdn.microsoft.com/bb7312a0-f851-44a4-8467-31bbe1a9ac41">MI_Class_GetServerName</a> .

