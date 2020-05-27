---
UID: NS:mi._MI_InstanceFT
title: MI_InstanceFT (mi.h)
description: A support structure used in the MI_Instance structure. Use the functions with the name prefix MI_Instance_ to manipulate these structures.
helpviewer_keywords: ["MI_InstanceFT","MI_InstanceFT structure [Windows Management Infrastructure (MI)]","mi/MI_InstanceFT","wmi_v2.mi_instanceft"]
old-location: wmi_v2\mi_instanceft.htm
tech.root: wmi_v2
ms.assetid: a8cd93b7-c9e0-415e-811a-33826e38417f
ms.date: 12/05/2018
ms.keywords: MI_InstanceFT, MI_InstanceFT structure [Windows Management Infrastructure (MI)], mi/MI_InstanceFT, wmi_v2.mi_instanceft
f1_keywords:
- mi/MI_InstanceFT
dev_langs:
- c++
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
targetos: Windows
req.typenames: MI_InstanceFT
req.redist: Windows Management Framework 3.0 on Windows Server 2008 R2 with SP1,     Windows 7 with SP1, and Windows Server 2008 with SP2
ms.custom: 19H1
---

# MI_InstanceFT structure


## -description


A support structure used in the <a href="https://docs.microsoft.com/windows/desktop/api/mi/ns-mi-mi_instance">MI_Instance</a> 
    structure. Use the functions with the name prefix <b>MI_Instance_</b> to manipulate 
    these structures.


## -struct-fields




### -field MI_Result

TBD 




#### - AddElement

Adds a new property to a dynamic instance. See 
       <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mi/nf-mi-mi_instance_addelement">MI_Instance_AddElement</a>.


#### - ClearElement

Clears the value of the named element (CIM property) and sets it to Null. See 
       <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mi/nf-mi-mi_instance_clearelement">MI_Instance_ClearElement</a>.


#### - ClearElementAt

Clears the value of the element (CIM property) at the specified index and sets it to Null. See 
       <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mi/nf-mi-mi_instance_clearelementat">MI_Instance_ClearElementAt</a>.


#### - Clone

Creates a copy of the specified instance on the heap. See 
       <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mi/nf-mi-mi_instance_clone">MI_Instance_Clone</a>.


#### - Delete

Deletes an instance that was created on the heap. See 
       <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mi/nf-mi-mi_instance_delete">MI_Instance_Delete</a>.


#### - Destruct

Deletes an instance that was created on the stack. See 
       <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mi/nf-mi-mi_instance_destruct">MI_Instance_Destruct</a>.


#### - GetClass

Gets the <a href="https://docs.microsoft.com/windows/desktop/api/mi/ns-mi-mi_class">MI_Class</a>associated with an instance. See 
       <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mi/nf-mi-mi_instance_getclass">MI_Instance_GetClass</a>.


#### - GetClassName

Gets the class name of the specified instance. See 
       <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mi/nf-mi-mi_instance_getclassname">MI_Instance_GetClassName</a>.


#### - GetElement

Gets the value of the named element (CIM property). See 
       <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mi/nf-mi-mi_instance_getelement">MI_Instance_GetElement</a>.


#### - GetElementAt

Gets the value of the element (CIM property) at the specified index. See 
       <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mi/nf-mi-mi_instance_getelementat">MI_Instance_GetElementAt</a>.


#### - GetElementCount

Gets the number of elements in an instance. See 
       <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mi/nf-mi-mi_instance_getelementcount">MI_Instance_GetElementCount</a>.


#### - GetNameSpace

Gets the namespace name of the specified instance. See 
       <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mi/nf-mi-mi_instance_getnamespace">MI_Instance_GetNameSpace</a>.


#### - GetServerName

Gets the server name from the specified instance. See 
       <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mi/nf-mi-mi_instance_getservername">MI_Instance_GetServerName</a>.


#### - IsA

Determines if the instance self is an instance of the class given by classDecl. See 
       <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mi/nf-mi-mi_instance_isa">MI_Instance_IsA</a>.


#### - SetElement

Set the value of the property with the given name in the given instance. See 
       <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mi/nf-mi-mi_instance_setelement">MI_Instance_SetElement</a>.


#### - SetElementAt

Set the value of the property at the given index of an instance. See 
       <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mi/nf-mi-mi_instance_setelementat">MI_Instance_SetElementAt</a>.


#### - SetNameSpace

Sets the namespace name of the specified instance. See 
       <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mi/nf-mi-mi_instance_setnamespace">MI_Instance_SetNameSpace</a>.


#### - SetServerName

Sets the server name of the specified instance. See 
       <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mi/nf-mi-mi_instance_setservername">MI_Instance_SetServerName</a>.

