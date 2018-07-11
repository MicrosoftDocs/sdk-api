---
UID: NF:mi.MI_Filter_Evaluate
title: MI_Filter_Evaluate function
author: windows-sdk-content
description: The provider calls this function to evaluate an instance against a given filter.
old-location: wmi_v2\mi_filter_evaluate.htm
old-project: wmi_v2
ms.assetid: b826f02d-3764-4f61-996f-42bf01ea44e2
ms.author: windowssdkdev
ms.date: 06/14/2018
ms.keywords: MI_Filter_Evaluate, MI_Filter_Evaluate function [Windows Management Infrastructure (MI)], mi/MI_Filter_Evaluate, wmi_v2.mi_filter_evaluate
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
tech.root: 
req.typenames: MI_Type
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mi.h
api_name:
 - MI_Filter_Evaluate
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# MI_Filter_Evaluate function


## -description


The provider calls this function to evaluate an instance against a given filter.


## -parameters




### -param self [in]

This is a pointer to the filter the instance will be evaluated against.


### -param instance [in]

This is a pointer to the instance to evaluate.


### -param result [out]

When the API completes, result indicates whether the instance matched the filter.


## -returns



This function returns MI_INLINE MI_Result MI_INLINE_CALL.



