---
UID: NF:mi.MI_Instance_Destruct
title: MI_Instance_Destruct function (mi.h)
description: Deletes an instance that was created on the stack or as a member of a structure.
helpviewer_keywords: ["MI_Instance_Destruct","MI_Instance_Destruct function [Windows Management Infrastructure (MI)]","mi/MI_Instance_Destruct","wmi_v2.mi_instance_destruct"]
old-location: wmi_v2\mi_instance_destruct.htm
tech.root: wmi_v2
ms.assetid: 2ecbf165-0918-489c-8e70-b48c31263aed
ms.date: 12/05/2018
ms.keywords: MI_Instance_Destruct, MI_Instance_Destruct function [Windows Management Infrastructure (MI)], mi/MI_Instance_Destruct, wmi_v2.mi_instance_destruct
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
 - MI_Instance_Destruct
 - mi/MI_Instance_Destruct
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
 - MI_Instance_Destruct
---

# MI_Instance_Destruct function


## -description

Deletes  an instance that was created on the stack or as a member of a structure.

## -parameters

### -param self [in, out]

Instance to be deleted.

## -returns

A value of the <a href="/windows/desktop/api/mi/ne-mi-mi_result">MI_Result</a> enumeration that specifies the function return code. This can be one of the following codes.

## -see-also

<a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_context_constructinstance">MI_Context_ConstructInstance</a>



<a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_context_constructparameters">MI_Context_ConstructParameters</a>



<a href="/windows/desktop/api/mi/ns-mi-mi_instance">MI_Instance</a>