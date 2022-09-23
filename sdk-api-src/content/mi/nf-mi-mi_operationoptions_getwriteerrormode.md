---
UID: NF:mi.MI_OperationOptions_GetWriteErrorMode
title: MI_OperationOptions_GetWriteErrorMode function (mi.h)
description: Sets the error reporting mode. (MI_OperationOptions_GetWriteErrorMode)
helpviewer_keywords: ["MI_CALLBACKMODE_INQUIRE","MI_CALLBACKMODE_REPORT","MI_OperationOptions_GetWriteErrorMode","MI_OperationOptions_GetWriteErrorMode function [Windows Management Infrastructure (MI)]","mi/MI_OperationOptions_GetWriteErrorMode","wmi_v2.mi_operationoptions_getwriteerrormode"]
old-location: wmi_v2\mi_operationoptions_getwriteerrormode.htm
tech.root: wmi_v2
ms.assetid: e2bfaa20-a389-4e52-b8dd-e06941cf7393
ms.date: 12/05/2018
ms.keywords: MI_CALLBACKMODE_INQUIRE, MI_CALLBACKMODE_REPORT, MI_OperationOptions_GetWriteErrorMode, MI_OperationOptions_GetWriteErrorMode function [Windows Management Infrastructure (MI)], mi/MI_OperationOptions_GetWriteErrorMode, wmi_v2.mi_operationoptions_getwriteerrormode
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
 - MI_OperationOptions_GetWriteErrorMode
 - mi/MI_OperationOptions_GetWriteErrorMode
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
 - MI_OperationOptions_GetWriteErrorMode
---

# MI_OperationOptions_GetWriteErrorMode function


## -description

Sets the error reporting mode.

## -parameters

### -param options [in]

<a href="/windows/desktop/api/mi/ns-mi-mi_operationoptions">MI_OperationOptions</a> structure.

### -param mode [out]

Returned MI_CallbackMode value.



#### MI_CALLBACKMODE_REPORT

Prompt will be passed back to the client in reporting mode, meaning the client is notified of the prompt but cannot respond to it and the server will automatically confirm the request.



#### MI_CALLBACKMODE_INQUIRE

Provider will block while the client is called back to ask if the operation should continue or not.

## -returns

A value of the <a href="/windows/desktop/api/mi/ne-mi-mi_result">MI_Result</a> enumeration that specifies the function return code. This can be one of the following codes.
