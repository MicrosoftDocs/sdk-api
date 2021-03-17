---
UID: NF:mi.MI_Instance_SetNameSpace
title: MI_Instance_SetNameSpace function (mi.h)
description: Sets the namespace name of the specified instance.
helpviewer_keywords: ["MI_Instance_SetNameSpace","MI_Instance_SetNameSpace function [Windows Management Infrastructure (MI)]","mi/MI_Instance_SetNameSpace","wmi_v2.mi_instance_setnamespace"]
old-location: wmi_v2\mi_instance_setnamespace.htm
tech.root: wmi_v2
ms.assetid: edf17b80-698b-43f3-9e03-5435638d3209
ms.date: 12/05/2018
ms.keywords: MI_Instance_SetNameSpace, MI_Instance_SetNameSpace function [Windows Management Infrastructure (MI)], mi/MI_Instance_SetNameSpace, wmi_v2.mi_instance_setnamespace
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
 - MI_Instance_SetNameSpace
 - mi/MI_Instance_SetNameSpace
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
 - MI_Instance_SetNameSpace
---

# MI_Instance_SetNameSpace function


## -description

Sets the namespace name of the specified instance.

## -parameters

### -param self [in, out]

Instance whose namespace name is to be set.

### -param nameSpace

A null-terminated string that represents the new namespace name.

## -returns

A value of the <a href="/windows/desktop/api/mi/ne-mi-mi_result">MI_Result</a> enumeration that specifies the function return code. This can be one of the following codes.

## -remarks

Namespace names must conform to the following examples:

<ul>
<li>root</li>
<li>root/cimv2</li>
<li>aaa/bbb/ccc</li>
</ul>