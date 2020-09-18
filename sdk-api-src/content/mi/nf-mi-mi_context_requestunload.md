---
UID: NF:mi.MI_Context_RequestUnload
title: MI_Context_RequestUnload function (mi.h)
description: Requests to unload the module or the provider.
helpviewer_keywords: ["MI_Context_RequestUnload","MI_Context_RequestUnload function [Windows Management Infrastructure (MI)]","mi/MI_Context_RequestUnload","wmi.mi_requestunload","wmi_v2.mi_context_requestunload"]
old-location: wmi_v2\mi_context_requestunload.htm
tech.root: wmi_v2
ms.assetid: 1eb20bff-326d-4d2f-9b71-a14ca8975597
ms.date: 12/05/2018
ms.keywords: MI_Context_RequestUnload, MI_Context_RequestUnload function [Windows Management Infrastructure (MI)], mi/MI_Context_RequestUnload, wmi.mi_requestunload, wmi_v2.mi_context_requestunload
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
 - MI_Context_RequestUnload
 - mi/MI_Context_RequestUnload
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
 - MI_Context_RequestUnload
---

# MI_Context_RequestUnload function


## -description

Requests to unload the module or the provider.

## -parameters

### -param context [in]

The request context.

## -returns

A value of the <a href="/windows/desktop/api/mi/ne-mi-mi_result">MI_Result</a> enumeration that specifies the function return code. This can be one of the following codes.

## -remarks

This function undoes a call to the <a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_context_refuseunload">MI_Context_RefuseUnload</a> function. It must use the same context that was used in that function.

## -see-also

<a href="/windows/desktop/api/mi/ns-mi-mi_context">MI_Context</a>



<a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_context_refuseunload">MI_Context_RefuseUnload</a>