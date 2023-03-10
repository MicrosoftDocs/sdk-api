---
UID: NF:mi.MI_Application_NewOperationOptions
title: MI_Application_NewOperationOptions function (mi.h)
description: Creates an MI_OperationOptions object that can be used with the operation functions on the MI_Session object.
helpviewer_keywords: ["MI_Application_NewOperationOptions","MI_Application_NewOperationOptions function [Windows Management Infrastructure (MI)]","mi/MI_Application_NewOperationOptions","wmi_v2.mi_application_newoperationoptions"]
old-location: wmi_v2\mi_application_newoperationoptions.htm
tech.root: wmi_v2
ms.assetid: 0b9f569b-bb32-4393-9fd2-9d5d601c2214
ms.date: 12/05/2018
ms.keywords: MI_Application_NewOperationOptions, MI_Application_NewOperationOptions function [Windows Management Infrastructure (MI)], mi/MI_Application_NewOperationOptions, wmi_v2.mi_application_newoperationoptions
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
 - MI_Application_NewOperationOptions
 - mi/MI_Application_NewOperationOptions
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
 - MI_Application_NewOperationOptions
---

# MI_Application_NewOperationOptions function


## -description

Creates an <a href="/windows/desktop/api/mi/ns-mi-mi_operationoptions">MI_OperationOptions</a> object that can be used with the operation functions on the <a href="/windows/desktop/api/mi/ns-mi-mi_session">MI_Session</a> object.

## -parameters

### -param application [in]

A pointer to a handle returned from the <a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_application_initializev1">MI_Application_Initialize</a> function.

### -param mustUnderstand

Specifies if the transport and provider are required to process the options being passed. This should be set to <b>MI_FALSE</b>. Setting this parameter to <b>MI_TRUE</b> can cause the operation to fail if the server cannot process one of the options.

### -param options [out]

A pointer to an options handle returned from this function.

## -returns

This function returns MI_INLINE MI_Result.

## -remarks

When you have finished using the object returned from this call, delete it by calling the <a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_operationoptions_delete">MI_OperationOptions_Delete</a> function.