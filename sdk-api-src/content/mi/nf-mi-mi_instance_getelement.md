---
UID: NF:mi.MI_Instance_GetElement
title: MI_Instance_GetElement function (mi.h)
description: Gets the value of the named element (CIM property).
helpviewer_keywords: ["MI_FLAG_IN","MI_FLAG_KEY","MI_FLAG_NULL","MI_FLAG_OUT","MI_Instance_GetElement","MI_Instance_GetElement function [Windows Management Infrastructure (MI)]","mi/MI_Instance_GetElement","wmi_v2.mi_instance_getelement"]
old-location: wmi_v2\mi_instance_getelement.htm
tech.root: wmi_v2
ms.assetid: 1e366cc5-0fb9-41c9-961c-07b076a18529
ms.date: 12/05/2018
ms.keywords: MI_FLAG_IN, MI_FLAG_KEY, MI_FLAG_NULL, MI_FLAG_OUT, MI_Instance_GetElement, MI_Instance_GetElement function [Windows Management Infrastructure (MI)], mi/MI_Instance_GetElement, wmi_v2.mi_instance_getelement
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
 - MI_Instance_GetElement
 - mi/MI_Instance_GetElement
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
 - MI_Instance_GetElement
---

# MI_Instance_GetElement function


## -description

Gets the value of the named element (CIM property).

## -parameters

### -param self [in]

Instance whose element value will be returned.

### -param name

A null-terminated string that represents the name of the element.

### -param value [out, optional]

Returned element value.

### -param type [out, optional]

Returned element value type.

### -param flags [out, optional]

Returned combination of the following values.



#### MI_FLAG_NULL (0x20000000)

Element value is <b>Null</b>.



#### MI_FLAG_KEY (0x0001000)

Element is a key.



#### MI_FLAG_IN (0x0002000)

The parameter is of type <b>In</b> and is passed into a method.



#### MI_FLAG_OUT (0x0004000)

The parameter is of type <b>Out</b> and is returned from a method.

### -param index [out, optional]

Returned zero-based index of the element.

## -returns

A value of the <a href="/windows/desktop/api/mi/ne-mi-mi_result">MI_Result</a> enumeration that specifies the function return code. This can be one of the following codes.

## -see-also

<a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_instance_addelement">MI_Instance_AddElement</a>



<a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_instance_clearelement">MI_Instance_ClearElement</a>



<a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_instance_setelement">MI_Instance_SetElement</a>