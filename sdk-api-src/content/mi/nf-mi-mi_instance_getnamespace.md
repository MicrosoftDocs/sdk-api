---
UID: NF:mi.MI_Instance_GetNameSpace
title: MI_Instance_GetNameSpace function (mi.h)
description: Gets the namespace name of the specified instance.
helpviewer_keywords: ["MI_Instance_GetNameSpace","MI_Instance_GetNameSpace function [Windows Management Infrastructure (MI)]","mi/MI_Instance_GetNameSpace","wmi_v2.mi_instance_getnamespace"]
old-location: wmi_v2\mi_instance_getnamespace.htm
tech.root: wmi_v2
ms.assetid: 885423d6-c247-4d45-a5fd-a1a18bd5e6e2
ms.date: 12/05/2018
ms.keywords: MI_Instance_GetNameSpace, MI_Instance_GetNameSpace function [Windows Management Infrastructure (MI)], mi/MI_Instance_GetNameSpace, wmi_v2.mi_instance_getnamespace
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
 - MI_Instance_GetNameSpace
 - mi/MI_Instance_GetNameSpace
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
 - MI_Instance_GetNameSpace
---

# MI_Instance_GetNameSpace function


## -description

Gets the namespace name of the specified instance.

## -parameters

### -param self [in]

Instance whose namespace name is to be returned.

### -param nameSpace

Returned namespace name.

## -returns

A value of the <a href="/windows/desktop/api/mi/ne-mi-mi_result">MI_Result</a> enumeration that specifies the function return code. This can be one of the following codes.