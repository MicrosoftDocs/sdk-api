---
UID: NF:mi.MI_Instance_GetClassName
title: MI_Instance_GetClassName function (mi.h)
description: Gets the class name of the specified instance.
helpviewer_keywords: ["MI_Instance_GetClassName","MI_Instance_GetClassName function [Windows Management Infrastructure (MI)]","mi/MI_Instance_GetClassName","wmi_v2.mi_instance_getclassname"]
old-location: wmi_v2\mi_instance_getclassname.htm
tech.root: wmi_v2
ms.assetid: d2129902-3a2d-479d-b83a-3582094b2fce
ms.date: 12/05/2018
ms.keywords: MI_Instance_GetClassName, MI_Instance_GetClassName function [Windows Management Infrastructure (MI)], mi/MI_Instance_GetClassName, wmi_v2.mi_instance_getclassname
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
 - MI_Instance_GetClassName
 - mi/MI_Instance_GetClassName
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
 - MI_Instance_GetClassName
---

# MI_Instance_GetClassName function


## -description

Gets the class name of the specified instance.

## -parameters

### -param self [in]

Instance whose class name will be returned.

### -param className

A pointer to a null-terminated string containing the returned class name.

## -returns

A value of the <a href="/windows/desktop/api/mi/ne-mi-mi_result">MI_Result</a> enumeration that specifies the function return code. This can be one of the following codes.

## -see-also

<a href="/windows/desktop/api/mi/ns-mi-mi_instance">MI_Instance</a>