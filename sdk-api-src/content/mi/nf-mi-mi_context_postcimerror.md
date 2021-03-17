---
UID: NF:mi.MI_Context_PostCimError
title: MI_Context_PostCimError function (mi.h)
description: Posts a return code and an error message (in the form of a CIM_Error object) to the server in response to a request.
helpviewer_keywords: ["MI_Context_PostCimError","MI_Context_PostCimError function [Windows Management Infrastructure (MI)]","mi/MI_Context_PostCimError","wmi.mi_postcimerror","wmi_v2.mi_context_postcimerror"]
old-location: wmi_v2\mi_context_postcimerror.htm
tech.root: wmi_v2
ms.assetid: 96ef9e97-467b-4b71-a7f9-4f640102e744
ms.date: 12/05/2018
ms.keywords: MI_Context_PostCimError, MI_Context_PostCimError function [Windows Management Infrastructure (MI)], mi/MI_Context_PostCimError, wmi.mi_postcimerror, wmi_v2.mi_context_postcimerror
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
 - MI_Context_PostCimError
 - mi/MI_Context_PostCimError
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
 - MI_Context_PostCimError
---

# MI_Context_PostCimError function


## -description

Posts a return code and an error message (in the form of a <a href="/windows/desktop/hyperv_v2/cim-error">CIM_Error</a> object) to the server in response to a request.

## -parameters

### -param context [in]

A pointer to the request context.

### -param error [in]

A pointer to a <a href="/windows/desktop/hyperv_v2/cim-error">CIM_Error</a> object to be posted to the server.

## -returns

This function returns MI_INLINE MI_Result MI_INLINE_CALL.

## -remarks

The <a href="/windows/desktop/hyperv_v2/cim-error">CIM_Error</a> instance that is returned in the <i>error</i> parameter can be compiled into your provider so you can initialize and then post it. Once an error has been posted, the context must not be used, as it becomes invalid at this point.

## -see-also

<a href="/windows/desktop/hyperv_v2/cim-error">CIM_Error</a>



<a href="/windows/desktop/api/mi/ns-mi-mi_context">MI_Context</a>



<a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_context_writecimerror">MI_Context_WriteCimError</a>



<a href="/windows/desktop/api/mi/ns-mi-mi_instance">MI_Instance</a>