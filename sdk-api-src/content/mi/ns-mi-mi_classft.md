---
UID: NS:mi._MI_ClassFT
title: MI_ClassFT (mi.h)
description: A support structure used in the MI_Class structure. Use the functions with the name prefix &quot;MI_Class_&quot; to manipulate these structures.
helpviewer_keywords: ["MI_ClassFT","MI_ClassFT structure [Windows Management Infrastructure (MI)]","mi/MI_ClassFT","wmi_v2.mi_classft"]
old-location: wmi_v2\mi_classft.htm
tech.root: wmi_v2
ms.assetid: 464dd009-5d99-483c-9e94-82ab07290189
ms.date: 12/05/2018
ms.keywords: MI_ClassFT, MI_ClassFT structure [Windows Management Infrastructure (MI)], mi/MI_ClassFT, wmi_v2.mi_classft
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
targetos: Windows
req.typenames: MI_ClassFT
req.redist: Windows Management Framework 3.0 on Windows Server 2008 R2 with SP1,     Windows 7 with SP1, and Windows Server 2008 with SP2
ms.custom: 19H1
f1_keywords:
 - _MI_ClassFT
 - mi/_MI_ClassFT
 - MI_ClassFT
 - mi/MI_ClassFT
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mi.h
api_name:
 - MI_ClassFT
---

## -description

A support structure used in the <a href="/windows/desktop/api/mi/ns-mi-mi_class">MI_Class</a> structure. 
     Use the functions with the name prefix "MI_Class_" to manipulate these structures.

## -struct-fields

### -field GetClassName

Retrieves the class name of the class. See 
       <a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_class_getclassname">MI_Class_GetClassName</a>.

### -field GetNameSpace

Retrieves the namespace of the class. See 
       <a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_class_getnamespace">MI_Class_GetNameSpace</a>.

### -field GetServerName

Retrieves the server name of the class. See 
       <a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_class_getservername">MI_Class_GetServerName</a> .

### -field GetElementCount

Retrieves the number of elements in a class. See 
       <a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_class_getelementcount">MI_Class_GetElementCount</a> .

### -field GetElement

Retrieves information about a named class element. See 
       <a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_class_getelement">MI_Class_GetElement</a>.

### -field GetElementAt

Retrieves information about a specific class element given the element index (Indexes start from 0). See 
       <a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_class_getelementat">MI_Class_GetElementAt</a>.

### -field GetClassQualifierSet

Retrieve an object from a class that allows the class qualifiers to be queried. See 
       <a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_class_getclassqualifierset">MI_Class_GetClassQualifierSet</a>.

### -field GetMethodCount

Retrieves the number of class methods. See 
       <a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_class_getmethodcount">MI_Class_GetMethodCount</a>.

### -field GetMethodAt

Get method information based on a method index. See 
       <a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_class_getmethodat">MI_Class_GetMethodAt</a>.

### -field GetMethod

Get method information based on a method name. See 
       <a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_class_getmethod">MI_Class_GetMethod</a>.

### -field GetParentClassName

Get the parent class name of the class. See 
       <a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_class_getparentclassname">MI_Class_GetParentClassName</a>.

### -field GetParentClass

Get the parent class for the specified class. See 
       <a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_class_getparentclass">MI_Class_GetParentClass</a>.

### -field Delete

Delete an <a href="/windows/desktop/api/mi/ns-mi-mi_class">MI_Class</a> object. See 
       <a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_class_delete">MI_Class_Delete</a>.

### -field Clone

Clones an <a href="/windows/desktop/api/mi/ns-mi-mi_class">MI_Class</a> object. See 
       <a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_class_clone">MI_Class_Clone</a>.
