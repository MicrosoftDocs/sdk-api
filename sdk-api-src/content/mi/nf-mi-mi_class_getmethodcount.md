---
UID: NF:mi.MI_Class_GetMethodCount
title: MI_Class_GetMethodCount function (mi.h)
description: Gets the number of methods in the class.
helpviewer_keywords: ["MI_Class_GetMethodCount","MI_Class_GetMethodCount function [Windows Management Infrastructure (MI)]","mi/MI_Class_GetMethodCount","wmi_v2.mi_class_getmethodcount"]
old-location: wmi_v2\mi_class_getmethodcount.htm
tech.root: wmi_v2
ms.assetid: 7190273e-bed5-4888-87c6-7e2d44aae703
ms.date: 12/05/2018
ms.keywords: MI_Class_GetMethodCount, MI_Class_GetMethodCount function [Windows Management Infrastructure (MI)], mi/MI_Class_GetMethodCount, wmi_v2.mi_class_getmethodcount
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
 - MI_Class_GetMethodCount
 - mi/MI_Class_GetMethodCount
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
 - MI_Class_GetMethodCount
---

# MI_Class_GetMethodCount function


## -description

Gets the number of methods in the class.

## -parameters

### -param self [in]

A pointer to the class from which to get the method count.

### -param count [out]

A pointer to the returned method count.

## -returns

This function returns MI_INLINE MI_Result.

