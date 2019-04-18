---
UID: NS:mi._MI_InstanceFT
title: MI_InstanceFT (mi.h)
author: windows-sdk-content
description: A support structure used in the MI_Instance structure. Use the functions with the name prefix MI_Instance_ to manipulate these structures.
old-location: wmi_v2\mi_instanceft.htm
tech.root: wmi_v2
ms.assetid: a8cd93b7-c9e0-415e-811a-33826e38417f
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: MI_InstanceFT, MI_InstanceFT structure [Windows Management Infrastructure (MI)], mi/MI_InstanceFT, wmi_v2.mi_instanceft
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
 - MI_InstanceFT
product: Windows
targetos: Windows
req.typenames: MI_InstanceFT
req.redist: Windows Management Framework 3.0 on Windows Server 2008 R2 with SP1,     Windows 7 with SP1, and Windows Server 2008 with SP2
ms.custom: 19H1
---

# MI_InstanceFT structure


## -description


A support structure used in the <a href="https://msdn.microsoft.com/3dce1817-7995-49e5-8cc0-ee9496665e5c">MI_Instance</a> 
    structure. Use the functions with the name prefix <b>MI_Instance_</b> to manipulate 
    these structures.


## -struct-fields




### -field MI_Result

TBD 




#### - AddElement

Adds a new property to a dynamic instance. See 
       <a href="https://msdn.microsoft.com/51a26894-f391-4281-9e06-2e70fb662aa2">MI_Instance_AddElement</a>.


#### - ClearElement

Clears the value of the named element (CIM property) and sets it to Null. See 
       <a href="https://msdn.microsoft.com/de945902-4b10-47d1-a374-a1aeab02a787">MI_Instance_ClearElement</a>.


#### - ClearElementAt

Clears the value of the element (CIM property) at the specified index and sets it to Null. See 
       <a href="https://msdn.microsoft.com/ef97bfa4-2e06-44b1-aa50-ce8c6a550c69">MI_Instance_ClearElementAt</a>.


#### - Clone

Creates a copy of the specified instance on the heap. See 
       <a href="https://msdn.microsoft.com/9c7a4659-5bc4-4d24-89bc-9da4f2bdf107">MI_Instance_Clone</a>.


#### - Delete

Deletes an instance that was created on the heap. See 
       <a href="https://msdn.microsoft.com/6370e464-b262-4c91-a3c8-889911df7965">MI_Instance_Delete</a>.


#### - Destruct

Deletes an instance that was created on the stack. See 
       <a href="https://msdn.microsoft.com/2ecbf165-0918-489c-8e70-b48c31263aed">MI_Instance_Destruct</a>.


#### - GetClass

Gets the <a href="https://msdn.microsoft.com/7f02e0fa-9e58-455d-9cf4-1d1244c44422">MI_Class</a>associated with an instance. See 
       <a href="https://msdn.microsoft.com/4799e9f0-f233-499f-acec-9041074eab42">MI_Instance_GetClass</a>.


#### - GetClassName

Gets the class name of the specified instance. See 
       <a href="https://msdn.microsoft.com/d2129902-3a2d-479d-b83a-3582094b2fce">MI_Instance_GetClassName</a>.


#### - GetElement

Gets the value of the named element (CIM property). See 
       <a href="https://msdn.microsoft.com/1e366cc5-0fb9-41c9-961c-07b076a18529">MI_Instance_GetElement</a>.


#### - GetElementAt

Gets the value of the element (CIM property) at the specified index. See 
       <a href="https://msdn.microsoft.com/4437162d-6320-4ec5-9a1c-b50dcc1516e3">MI_Instance_GetElementAt</a>.


#### - GetElementCount

Gets the number of elements in an instance. See 
       <a href="https://msdn.microsoft.com/a378bde1-c164-4905-82f8-f771f8da60ba">MI_Instance_GetElementCount</a>.


#### - GetNameSpace

Gets the namespace name of the specified instance. See 
       <a href="https://msdn.microsoft.com/885423d6-c247-4d45-a5fd-a1a18bd5e6e2">MI_Instance_GetNameSpace</a>.


#### - GetServerName

Gets the server name from the specified instance. See 
       <a href="https://msdn.microsoft.com/773b2cb9-9296-4da9-8c13-288524bfccd5">MI_Instance_GetServerName</a>.


#### - IsA

Determines if the instance self is an instance of the class given by classDecl. See 
       <a href="https://msdn.microsoft.com/53fe80b3-cd34-4dee-a474-ced784d61682">MI_Instance_IsA</a>.


#### - SetElement

Set the value of the property with the given name in the given instance. See 
       <a href="https://msdn.microsoft.com/581f8d9f-5421-44ab-a3e2-dfb536a35c2c">MI_Instance_SetElement</a>.


#### - SetElementAt

Set the value of the property at the given index of an instance. See 
       <a href="https://msdn.microsoft.com/4070af24-b7f9-4484-ab13-d3a52c9e55a0">MI_Instance_SetElementAt</a>.


#### - SetNameSpace

Sets the namespace name of the specified instance. See 
       <a href="https://msdn.microsoft.com/edf17b80-698b-43f3-9e03-5435638d3209">MI_Instance_SetNameSpace</a>.


#### - SetServerName

Sets the server name of the specified instance. See 
       <a href="https://msdn.microsoft.com/34864c69-091f-4dbd-9d56-e43f8d218b09">MI_Instance_SetServerName</a>.

