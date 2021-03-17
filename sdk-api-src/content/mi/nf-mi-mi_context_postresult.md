---
UID: NF:mi.MI_Context_PostResult
title: MI_Context_PostResult function (mi.h)
description: Posts the final terminating result code back to the client (through the server) in response to a request.
helpviewer_keywords: ["MI_Context_PostResult","MI_Context_PostResult function [Windows Management Infrastructure (MI)]","mi/MI_Context_PostResult","wmi.mi_postresult","wmi_v2.mi_context_postresult"]
old-location: wmi_v2\mi_context_postresult.htm
tech.root: wmi_v2
ms.assetid: e890ebab-f243-40eb-8a56-a771475929bb
ms.date: 12/05/2018
ms.keywords: MI_Context_PostResult, MI_Context_PostResult function [Windows Management Infrastructure (MI)], mi/MI_Context_PostResult, wmi.mi_postresult, wmi_v2.mi_context_postresult
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
 - MI_Context_PostResult
 - mi/MI_Context_PostResult
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
 - MI_Context_PostResult
---

# MI_Context_PostResult function


## -description

Posts the final terminating result code back to the client (through the server) in response to a request.

## -parameters

### -param context [in]

Request context.

### -param result

Result code to post to the server.

## -returns

This function returns MI_INLINE MI_Result MI_INLINE_CALL.

## -remarks

All calls to the <a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_context_postindication">MI_Context_PostIndication</a> and <a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_context_postinstance">MI_Context_PostInstance</a> functions must be complete before calling this function. When this function is called, the lifetime of the request context is terminated; the context becomes invalid, and no additional calls can be made on the context.

## -see-also

<a href="/windows/desktop/api/mi/ns-mi-mi_context">MI_Context</a>



<a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_context_postindication">MI_Context_PostIndication</a>



<a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_context_postinstance">MI_Context_PostInstance</a>