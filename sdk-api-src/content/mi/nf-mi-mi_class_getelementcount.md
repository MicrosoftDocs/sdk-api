---
UID: NF:mi.MI_Class_GetElementCount
title: MI_Class_GetElementCount function (mi.h)
description: Gets the number of elements in a class.
helpviewer_keywords: ["MI_Class_GetElementCount","MI_Class_GetElementCount function [Windows Management Infrastructure (MI)]","mi/MI_Class_GetElementCount","wmi_v2.mi_class_getelementcount"]
old-location: wmi_v2\mi_class_getelementcount.htm
tech.root: wmi_v2
ms.assetid: f6db81ca-0411-4693-8bcc-830d4fd757ca
ms.date: 12/05/2018
ms.keywords: MI_Class_GetElementCount, MI_Class_GetElementCount function [Windows Management Infrastructure (MI)], mi/MI_Class_GetElementCount, wmi_v2.mi_class_getelementcount
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
 - MI_Class_GetElementCount
 - mi/MI_Class_GetElementCount
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
 - MI_Class_GetElementCount
---

# MI_Class_GetElementCount function


## -description

Gets the number of elements in a class.

## -parameters

### -param self [in]

A pointer to the class from which to get the element count.

### -param count [out]

A pointer to the variable to receive the returned element count.

## -returns

This function returns MI_INLINE MI_Result.

