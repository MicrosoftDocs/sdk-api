---
UID: NF:mi.MI_Context_GetNumberOption
title: MI_Context_GetNumberOption function (mi.h)
description: Gets the numeric option that the client sets, based on the operation name.
helpviewer_keywords: ["MI_Context_GetNumberOption","MI_Context_GetNumberOption function [Windows Management Infrastructure (MI)]","mi/MI_Context_GetNumberOption","wmi.mi_getnumberoption","wmi_v2.mi_context_getnumberoption"]
old-location: wmi_v2\mi_context_getnumberoption.htm
tech.root: wmi_v2
ms.assetid: 862a44b9-a6bd-4433-a7da-9309392a946c
ms.date: 12/05/2018
ms.keywords: MI_Context_GetNumberOption, MI_Context_GetNumberOption function [Windows Management Infrastructure (MI)], mi/MI_Context_GetNumberOption, wmi.mi_getnumberoption, wmi_v2.mi_context_getnumberoption
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
 - MI_Context_GetNumberOption
 - mi/MI_Context_GetNumberOption
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
 - MI_Context_GetNumberOption
---

# MI_Context_GetNumberOption function


## -description

Gets the numeric option that the client sets, based on the operation name.

## -parameters

### -param context [in]

A pointer to the request context.

### -param name [in]

The name of the option to get.

### -param value [out, optional]

A pointer to the returned option value. This parameter is optional.

## -returns

A value of the <a href="/windows/desktop/api/mi/ne-mi-mi_result">MI_Result</a> enumeration that specifies the function return code. This can be one of the following codes.