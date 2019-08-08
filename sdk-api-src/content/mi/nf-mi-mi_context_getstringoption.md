---
UID: NF:mi.MI_Context_GetStringOption
title: MI_Context_GetStringOption function (mi.h)
author: windows-sdk-content
description: Gets the string option that the client sets, based on the operation name.
old-location: wmi_v2\mi_context_getstringoption.htm
tech.root: wmi_v2
ms.assetid: ef6fa103-7421-4c66-902d-c5a731abaa54
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: MI_Context_GetStringOption, MI_Context_GetStringOption function [Windows Management Infrastructure (MI)], mi/MI_Context_GetStringOption, wmi.mi_getstringoption, wmi_v2.mi_context_getstringoption
ms.topic: function
f1_keywords:
- mi/MI_Context_GetStringOption
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
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- Mi.h
api_name:
- MI_Context_GetStringOption
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Management Framework 3.0 on Windows Server 2008 R2 with SP1, Windows 7 with SP1, and Windows Server 2008 with SP2
ms.custom: 19H1
---

# MI_Context_GetStringOption function


## -description


Gets the string option that the client sets, based on the operation name.


## -parameters




### -param context [in]

A pointer to the request context.


### -param name [in]

The name of the option to get.


### -param value

A pointer to the returned option value.


## -returns



A value of the <a href="https://docs.microsoft.com/windows/desktop/api/mi/ne-mi-mi_result">MI_Result</a> enumeration that specifies the function return code. This can be one of the following codes.




## -remarks



The returned string does not need to be deleted. The string is valid until the provider returns the final result for this operation.



