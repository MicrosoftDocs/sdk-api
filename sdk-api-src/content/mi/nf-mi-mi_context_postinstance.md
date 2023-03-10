---
UID: NF:mi.MI_Context_PostInstance
title: MI_Context_PostInstance function (mi.h)
description: Posts an instance back to the client (through the server) in response to a request.
helpviewer_keywords: ["MI_Context_PostInstance","MI_Context_PostInstance function [Windows Management Infrastructure (MI)]","mi/MI_Context_PostInstance","wmi.mi_postinstance","wmi_v2.mi_context_postinstance"]
old-location: wmi_v2\mi_context_postinstance.htm
tech.root: wmi_v2
ms.assetid: b7c5e677-5b49-48b8-8273-4fd04c2f4a90
ms.date: 12/05/2018
ms.keywords: MI_Context_PostInstance, MI_Context_PostInstance function [Windows Management Infrastructure (MI)], mi/MI_Context_PostInstance, wmi.mi_postinstance, wmi_v2.mi_context_postinstance
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
 - MI_Context_PostInstance
 - mi/MI_Context_PostInstance
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
 - MI_Context_PostInstance
---

# MI_Context_PostInstance function


## -description

Posts an instance back to the client (through the server) in response to a request.

## -parameters

### -param context [in]

Request context.

### -param instance [in]

Instance to be posted to the server.

## -returns

This function returns MI_INLINE MI_Result MI_INLINE_CALL.

## -remarks

There will be posting functions automatically generated for the indication class (for example, className_Post), and they should be called here.

The server is responsible for copying the instance so the provider is free to dispose of the instance afterwards using the <a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_instance_delete">MI_Instance_Delete</a> function.

## -see-also

<a href="/windows/desktop/api/mi/ns-mi-mi_context">MI_Context</a>



<a href="/windows/desktop/api/mi/ns-mi-mi_instance">MI_Instance</a>



<a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_instance_delete">MI_Instance_Delete</a>