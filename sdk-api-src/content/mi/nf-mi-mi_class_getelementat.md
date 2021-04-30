---
UID: NF:mi.MI_Class_GetElementAt
title: MI_Class_GetElementAt function (mi.h)
description: Gets details of a class element based on the element index.
helpviewer_keywords: ["MI_Class_GetElementAt","MI_Class_GetElementAt function [Windows Management Infrastructure (MI)]","MI_FLAG_ABSTRACT","MI_FLAG_ADOPT","MI_FLAG_ANY","MI_FLAG_ASSOCIATION","MI_FLAG_BORROW","MI_FLAG_CLASS","MI_FLAG_DISABLEOVERRIDE","MI_FLAG_ENABLEOVERRIDE","MI_FLAG_EXPENSIVE","MI_FLAG_IN","MI_FLAG_INDICATION","MI_FLAG_KEY","MI_FLAG_METHOD","MI_FLAG_NOT_MODIFIED","MI_FLAG_NULL","MI_FLAG_OUT","MI_FLAG_PARAMETER","MI_FLAG_PROPERTY","MI_FLAG_READONLY","MI_FLAG_REFERENCE","MI_FLAG_REQUIRED","MI_FLAG_RESTRICTED","MI_FLAG_STATIC","MI_FLAG_STREAM","MI_FLAG_TERMINAL","MI_FLAG_TOSUBCLASS","MI_FLAG_TRANSLATABLE","MI_FLAG_VERSION","mi/MI_Class_GetElementAt","wmi_v2.mi_class_getelementat"]
old-location: wmi_v2\mi_class_getelementat.htm
tech.root: wmi_v2
ms.assetid: f5479cc7-e3f6-447f-a8f8-dc08f3babe54
ms.date: 12/05/2018
ms.keywords: MI_Class_GetElementAt, MI_Class_GetElementAt function [Windows Management Infrastructure (MI)], MI_FLAG_ABSTRACT, MI_FLAG_ADOPT, MI_FLAG_ANY, MI_FLAG_ASSOCIATION, MI_FLAG_BORROW, MI_FLAG_CLASS, MI_FLAG_DISABLEOVERRIDE, MI_FLAG_ENABLEOVERRIDE, MI_FLAG_EXPENSIVE, MI_FLAG_IN, MI_FLAG_INDICATION, MI_FLAG_KEY, MI_FLAG_METHOD, MI_FLAG_NOT_MODIFIED, MI_FLAG_NULL, MI_FLAG_OUT, MI_FLAG_PARAMETER, MI_FLAG_PROPERTY, MI_FLAG_READONLY, MI_FLAG_REFERENCE, MI_FLAG_REQUIRED, MI_FLAG_RESTRICTED, MI_FLAG_STATIC, MI_FLAG_STREAM, MI_FLAG_TERMINAL, MI_FLAG_TOSUBCLASS, MI_FLAG_TRANSLATABLE, MI_FLAG_VERSION, mi/MI_Class_GetElementAt, wmi_v2.mi_class_getelementat
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
req.redist: Windows Management Framework 3.0 on Windows Server 2008 R2 with SP1, Windows 7 with SP1, and Windows Server 2008 with SP2
ms.custom: 19H1
f1_keywords:
 - MI_Class_GetElementAt
 - mi/MI_Class_GetElementAt
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
 - MI_Class_GetElementAt
---

# MI_Class_GetElementAt function


## -description

Gets details of a class element based on the element index.

## -parameters

### -param self [in]

A pointer to the class object from which the element is to be retrieved.

### -param index

Zero-based index of the element to retrieve.

### -param name

A pointer to the pointer to the variable to receive the returned name of the element.  The memory associated with the name is valid until the class object is deleted. When you have finished using the class object, delete it by calling the <a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_class_delete">MI_Class_Delete</a> function. If this information is not needed, pass <b>NULL</b> for this parameter.

### -param value [out, optional]

A pointer to the variable to receive the returned default value for the element.  The value is valid for the lifetime of the class object; the value does not need to be deleted. If this information is not needed, pass <b>NULL</b> for this parameter.

### -param valueExists [out, optional]

A pointer to the variable to receive the returned Boolean value that indicates whether a default value exits for the specified element. <b>MI_TRUE</b> if a default value exits; otherwise, <b>MI_FALSE</b>. If this information is not needed, pass <b>NULL</b> for this parameter.

### -param type [out, optional]

A pointer to the variable to receive the returned value of the <a href="/windows/desktop/api/mi/ne-mi-mi_type">MI_Type</a> enumeration that specifies the data type. This parameter is optional. If this information is not needed, pass <b>NULL</b> for this parameter.

### -param referenceClass

The class of the reference (if the element is a strongly typed reference) or the class name (if the element is a strongly typed embedded instance).

### -param qualifierSet [out, optional]

A pointer to the variable that receives the returned qualifier set.  This parameter is optional. The qualifier set exists for the lifetime of the class object. If this information is not needed, pass <b>NULL</b> for this parameter.

### -param flags [out, optional]

A pointer to the variable to receive the returned flag values that describe various aspects of the element. This parameter is optional. The returned flag values can be any combination of the following MI_FLAG_* values, with the exception of certain groups of mutually exclusive flags.



#### MI_FLAG_ABSTRACT (131072 (0x20000))

A class flag that indicates that the class is abstract. This flag is applicable only when used in conjunction with the <b>MI_FLAG_CLASS</b> flag, and the flag is mutually exclusive with the <b>MI_FLAG_TERMINAL</b> flag.



#### MI_FLAG_ADOPT (2147483648 (0x80000000))

A property flag used while adding and setting properties on an <a href="/windows/desktop/api/mi/ns-mi-mi_instance">MI_Instance</a> structure to indicate that the instance will adopt the pointer and will be responsible for deleting it. This flag is mutually exclusive with the <b>MI_FLAG_BORROW</b> flag.



#### MI_FLAG_ANY (127 (0x7F))

A bitmask used to filter out these CIM meta-type (qualifier scope) flags.

<ul>
<li><b>MI_FLAG_CLASS</b></li>
<li><b>MI_FLAG_METHOD</b></li>
<li><b>MI_FLAG_PROPERTY</b></li>
<li><b>MI_FLAG_PARAMETER</b></li>
<li><b>MI_FLAG_ASSOCIATION</b></li>
<li><b>MI_FLAG_INDICATION</b></li>
<li><b>MI_FLAG_REFERENCE</b></li>
</ul>


#### MI_FLAG_ASSOCIATION (16 (0x10))

A CIM meta-type used in the <a href="/windows/desktop/api/mi/ns-mi-mi_classdecl">MI_ClassDecl</a> structure to indicate that a class structure is also an association class structure. This flag is mutually exclusive with other CIM meta-type (qualifier scope) flags.



#### MI_FLAG_BORROW (1073741824 (0x40000000))

A property flag used while adding and setting properties on an <a href="/windows/desktop/api/mi/ns-mi-mi_instance">MI_Instance</a> structure to indicate that the instance will not copy the value. The value must stay valid until the instance is deleted. This flag is mutually exclusive with the <b>MI_FLAG_ADOPT</b> flag.



#### MI_FLAG_CLASS (1 (0x1))

A CIM meta-type used in the <a href="/windows/desktop/api/mi/ns-mi-mi_classdecl">MI_ClassDecl</a> structure to indicate a structure describing a class. This flag is mutually exclusive with other CIM meta-type (qualifier scope) flags.



#### MI_FLAG_DISABLEOVERRIDE (256 (0x100))

A qualifier flag flavor to indicate that the qualifier cannot be overridden. This flag is mutually exclusive with the <b>MI_FLAG_ENABLEOVERRIDE</b> flag.



#### MI_FLAG_ENABLEOVERRIDE (128 (0x80))

A qualifier flag flavor to indicate that the qualifier can be overridden. This flag is mutually exclusive with the <b>MI_FLAG_DISABLEOVERRIDE</b> flag.



#### MI_FLAG_EXPENSIVE (524288 (0x80000))

A property flag that indicates the property is expensive. A provider does not need to supply expensive properties unless the client asks for it, although most engines and clients do not support this concept and all properties are always returned. This flag is applicable only when used in conjunction with the <b>MI_FLAG_PROPERTY</b> flag.



#### MI_FLAG_IN (8192 (0x2000))

A parameter flag that indicates that the parameter is of type In and is passed into the method. This flag is applicable only when used in conjunction with the <b>MI_FLAG_PARAMETER</b> flag.



#### MI_FLAG_INDICATION (32 (0x20))

A CIM meta-type used in the <a href="/windows/desktop/api/mi/ns-mi-mi_classdecl">MI_ClassDecl</a> structure to indicate that a class structure is also an indication class structure. This flag is mutually exclusive with other CIM meta-type (qualifier scope) flags.



#### MI_FLAG_KEY (4096 (0x1000))

A property flag that indicates that the element is a key property. This flag is applicable only when used in conjunction with the <b>MI_FLAG_PROPERTY</b> flag.



#### MI_FLAG_METHOD (2 (0x2))

A CIM meta-type used in the MI_MethodDecl structure to indicate a structure describing a method. This flag is mutually exclusive with other CIM meta-type (qualifier scope) flags.



#### MI_FLAG_NOT_MODIFIED (33554432 (0x2000000))

A flag that indicates that the property is not modified.



#### MI_FLAG_NULL (536870912 (0x20000000))

A flag that indicates that a property value or method parameter value is null.



#### MI_FLAG_OUT (16384 (0x4000))

A parameter flag that indicates that the parameter is of type Out and is returned from the method. This flag is applicable only when used in conjunction with the <b>MI_FLAG_PARAMETER</b> flag.



#### MI_FLAG_PARAMETER (8 (0x8))

A CIM meta-type used in the <a href="/windows/desktop/api/mi/ns-mi-mi_parameterdecl">MI_ParameterDecl</a> structure to indicate a structure describing a parameter. This flag is mutually exclusive with other CIM meta-type (qualifier scope) flags.



#### MI_FLAG_PROPERTY (4 (0x4))

A CIM meta-type used in the <a href="/windows/desktop/api/mi/ns-mi-mi_propertydecl">MI_PropertyDecl</a> structure to indicate a structure describing a property. This flag is mutually exclusive with other CIM meta-type (qualifier scope) flags.



#### MI_FLAG_READONLY (2097152 (0x200000))

A property flag that indicates that the property can only be read and cannot be written to. This flag is applicable only when used in conjunction with the <b>MI_FLAG_PROPERTY</b> flag.



#### MI_FLAG_REFERENCE (64 (0x40))

A CIM meta-type used in the <a href="/windows/desktop/api/mi/ns-mi-mi_qualifierdecl">MI_QualifierDecl</a> structure in the <b>scope</b> field to indicate a structure describing a pointer to other instances. This flag is mutually exclusive with other CIM meta-type (qualifier scope) flags.



#### MI_FLAG_REQUIRED (32768 (0x8000))

A parameter flag that indicates that the parameter must be specified. This flag is applicable only when used in conjunction with the <b>MI_FLAG_PARAMETER</b> flag.



#### MI_FLAG_RESTRICTED (512 (0x200))

A qualifier flavor that states that the qualifier will not be propagated to a derived class. The qualifier applies only to the class in which it is declared. This flag is mutually exclusive with the <b>MI_FLAG_TOSUBCLASS</b> flag.



#### MI_FLAG_STATIC (65536 (0x10000))

A flag that is used on methods to indicate that the element is static and does not need an instance specifying the key to invoke it.



#### MI_FLAG_STREAM (1048576 (0x100000))

A flag that indicates that a method parameter will be streamed back to the client from the provider. This flag is applicable only when used in conjunction with the <b>MI_FLAG_PARAMETER</b> flag.



#### MI_FLAG_TERMINAL (262144 (0x40000))

A class flag that indicates that the class cannot be derived from. This flag is applicable only when used in conjunction with the <b>MI_FLAG_CLASS</b> flag, and the flag is mutually exclusive with the <b>MI_FLAG_ABSTRACT</b> flag.



#### MI_FLAG_TOSUBCLASS (1024 (0x400))

A qualifier flavor that states that the class qualifier is inherited automatically by any subclass. This flag is mutually exclusive with the <b>MI_FLAG_RESTRICTED</b> flag.



#### MI_FLAG_TRANSLATABLE (2048 (0x800))

A qualifier flavor that indicates that there may be different languages associated with the element. Translatable qualifiers will be treated such that strings and values can be localized in different languages.



#### MI_FLAG_VERSION (469762048 (0x1C000000))

Three bits reserved by the infrastructure to handle future versioning changes.

## -returns

This function returns MI_INLINE MI_Result.

## -remarks

All element information is read-only. The information returned is valid until the class is deleted.