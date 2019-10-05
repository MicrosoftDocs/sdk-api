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
f1_keywords:
- mi/MI_ClassFT
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
- MI_ClassFT
targetos: Windows
req.typenames: MI_ClassFT
req.redist: Windows Management Framework 3.0 on Windows Server 2008 R2 with SP1,     Windows 7 with SP1, and Windows Server 2008 with SP2
ms.custom: 19H1
---

# MI_ClassFT structure


## -description


A support structure used in the <a href="https://docs.microsoft.com/windows/desktop/api/mi/ns-mi-mi_class">MI_Class</a> structure. 
     Use the functions with the name prefix "MI_Class_" to manipulate these structures.


## -struct-fields




### -field MI_Result

TBD 




#### - Clone

Clones an <a href="https://docs.microsoft.com/windows/desktop/api/mi/ns-mi-mi_class">MI_Class</a> object. See 
       <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mi/nf-mi-mi_class_clone">MI_Class_Clone</a>.


#### - Delete

Delete an <a href="https://docs.microsoft.com/windows/desktop/api/mi/ns-mi-mi_class">MI_Class</a> object. See 
       <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mi/nf-mi-mi_class_delete">MI_Class_Delete</a>.


#### - GetClassName

Retrieves the class name of the class. See 
       <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mi/nf-mi-mi_class_getclassname">MI_Class_GetClassName</a>.


#### - GetClassQualifierSet

Retrieve an object from a class that allows the class qualifiers to be queried. See 
       <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mi/nf-mi-mi_class_getclassqualifierset">MI_Class_GetClassQualifierSet</a>.


#### - GetElement

Retrieves information about a named class element. See 
       <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mi/nf-mi-mi_class_getelement">MI_Class_GetElement</a>.


#### - GetElementAt

Retrieves information about a specific class element given the element index (Indexes start from 0). See 
       <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mi/nf-mi-mi_class_getelementat">MI_Class_GetElementAt</a>.


#### - GetElementCount

Retrieves the number of elements in a class. See 
       <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mi/nf-mi-mi_class_getelementcount">MI_Class_GetElementCount</a> .


#### - GetMethod

Get method information based on a method name. See 
       <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mi/nf-mi-mi_class_getmethod">MI_Class_GetMethod</a>.


#### - GetMethodAt

Get method information based on a method index. See 
       <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mi/nf-mi-mi_class_getmethodat">MI_Class_GetMethodAt</a>.


#### - GetMethodCount

Retrieves the number of class methods. See 
       <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mi/nf-mi-mi_class_getmethodcount">MI_Class_GetMethodCount</a>.


#### - GetNameSpace

Retrieves the namespace of the class. See 
       <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mi/nf-mi-mi_class_getnamespace">MI_Class_GetNameSpace</a>.


#### - GetParentClass

Get the parent class for the specified class. See 
       <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mi/nf-mi-mi_class_getparentclass">MI_Class_GetParentClass</a>.


#### - GetParentClassName

Get the parent class name of the class. See 
       <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mi/nf-mi-mi_class_getparentclassname">MI_Class_GetParentClassName</a>.


#### - GetServerName

Retrieves the server name of the class. See 
       <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mi/nf-mi-mi_class_getservername">MI_Class_GetServerName</a> .

