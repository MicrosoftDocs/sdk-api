---
UID: NF:mi.MI_Instance_IsA
title: MI_Instance_IsA function (mi.h)
description: Determines if the instance self is an instance of the class given by classDecl.
helpviewer_keywords: ["MI_Instance_IsA","MI_Instance_IsA function [Windows Management Infrastructure (MI)]","mi/MI_Instance_IsA","wmi_v2.mi_instance_isa"]
old-location: wmi_v2\mi_instance_isa.htm
tech.root: wmi_v2
ms.assetid: 53fe80b3-cd34-4dee-a474-ced784d61682
ms.date: 12/05/2018
ms.keywords: MI_Instance_IsA, MI_Instance_IsA function [Windows Management Infrastructure (MI)], mi/MI_Instance_IsA, wmi_v2.mi_instance_isa
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
 - MI_Instance_IsA
 - mi/MI_Instance_IsA
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
 - MI_Instance_IsA
---

# MI_Instance_IsA function


## -description

Determines if the instance <i>self</i> is an instance of the class given by <i>classDecl</i>.

## -parameters

### -param self [in]

Instance to compare.

### -param classDecl [in]

Class declaration to compare.

### -param flag [out]

Returned value that is set to <b>MI_TRUE</b> if <i>self</i> is an instance of <i>classDecl</i> or if the actual class of the instance inherits from the specified class.  Otherwise, it is set to <b>MI_FALSE</b>.

## -returns

A value of the <a href="/windows/desktop/api/mi/ne-mi-mi_result">MI_Result</a> enumeration that specifies the function return code. This can be one of the following codes.