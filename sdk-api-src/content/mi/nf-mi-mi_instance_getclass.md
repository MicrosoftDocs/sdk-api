---
UID: NF:mi.MI_Instance_GetClass
title: MI_Instance_GetClass function (mi.h)
description: Gets the MI_Class associated with an instance.
helpviewer_keywords: ["MI_Instance_GetClass","MI_Instance_GetClass function [Windows Management Infrastructure (MI)]","mi/MI_Instance_GetClass","wmi_v2.mi_instance_getclass"]
old-location: wmi_v2\mi_instance_getclass.htm
tech.root: wmi_v2
ms.assetid: 4799e9f0-f233-499f-acec-9041074eab42
ms.date: 12/05/2018
ms.keywords: MI_Instance_GetClass, MI_Instance_GetClass function [Windows Management Infrastructure (MI)], mi/MI_Instance_GetClass, wmi_v2.mi_instance_getclass
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
req.typenames: 
req.redist: Windows Management Framework 3.0 on Windows Server 2008 R2 with SP1,     Windows 7 with SP1, and Windows Server 2008 with SP2
ms.custom: 19H1
f1_keywords:
 - MI_Instance_GetClass
 - mi/MI_Instance_GetClass
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
 - MI_Instance_GetClass
---

# MI_Instance_GetClass function


## -description

Gets the <a href="/windows/desktop/api/mi/ns-mi-mi_class">MI_Class</a> associated with an 
     instance.

## -parameters

### -param self [in]

A pointer to an instance whose <a href="/windows/desktop/api/mi/ns-mi-mi_class">MI_Class</a> structure is 
      to be retrieved.

### -param instanceClass

Returned <a href="/windows/desktop/api/mi/ns-mi-mi_class">MI_Class</a>. This 
      <b>MI_Class</b> wraps the 
      <a href="/windows/desktop/api/mi/ns-mi-mi_classdecl">MI_ClassDecl</a> field inside the 
      <a href="/windows/desktop/api/mi/ns-mi-mi_instance">MI_Instance</a> and does not retrieve anything from the 
      server. This returned class should be deleted via 
      <a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_class_delete">MI_Class_Delete</a>.

## -returns

A value of the <a href="/windows/desktop/api/mi/ne-mi-mi_result">MI_Result</a> enumeration that specifies 
      the function return code. This can be one of the following codes.

## -remarks

Different types of classes exist. A dynamic instance has a very flat class declaration with no real 
    qualifiers. Certain 
    <a href="/previous-versions/windows/desktop/wmi_v2/mi-flags">flags</a> in to 
    session objects can also change the type of runtime type information (RTTI) that is returned, such that it has 
    none (types are all strings, flat structure, no qualifiers), basic (types of properties should be correct, but 
    they are flat-structured without qualifiers), standard (best effort at creating hierarchy, but overloaded 
    properties may not show original type in parent class), and full, which is an accurate class declaration. 
    Therefore, how an instance is created or retrieved will depend on the accuracy of the class declaration.

## -see-also

<a href="/windows/desktop/api/mi/ns-mi-mi_class">MI_Class</a>



<a href="/windows/desktop/api/mi/ns-mi-mi_classdecl">MI_ClassDecl</a>



<a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_class_delete">MI_Class_Delete</a>



<a href="/windows/desktop/api/mi/ns-mi-mi_instance">MI_Instance</a>