---
UID: NF:mi.MI_Instance_Clone
title: MI_Instance_Clone function (mi.h)
description: Creates a copy of the specified instance on the heap.
helpviewer_keywords: ["MI_Instance_Clone","MI_Instance_Clone function [Windows Management Infrastructure (MI)]","mi/MI_Instance_Clone","wmi_v2.mi_instance_clone"]
old-location: wmi_v2\mi_instance_clone.htm
tech.root: wmi_v2
ms.assetid: 9c7a4659-5bc4-4d24-89bc-9da4f2bdf107
ms.date: 12/05/2018
ms.keywords: MI_Instance_Clone, MI_Instance_Clone function [Windows Management Infrastructure (MI)], mi/MI_Instance_Clone, wmi_v2.mi_instance_clone
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
 - MI_Instance_Clone
 - mi/MI_Instance_Clone
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
 - MI_Instance_Clone
---

# MI_Instance_Clone function


## -description

Creates a copy of the specified instance on the heap.

## -parameters

### -param self [in]

Instance to be cloned.

### -param newInstance

Returned instance. This should be deleted via <a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_instance_delete">MI_Instance_Delete</a>.

## -returns

A value of the <a href="/windows/desktop/api/mi/ne-mi-mi_result">MI_Result</a> enumeration that specifies the function return code. This can be one of the following codes.