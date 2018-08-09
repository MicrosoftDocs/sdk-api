---
UID: NF:mi.MI_OperationOptions_GetWriteErrorMode
title: MI_OperationOptions_GetWriteErrorMode function
author: windows-sdk-content
description: Sets the error reporting mode.
old-location: wmi_v2\mi_operationoptions_getwriteerrormode.htm
old-project: wmi_v2
ms.assetid: e2bfaa20-a389-4e52-b8dd-e06941cf7393
ms.author: windowssdkdev
ms.date: 08/03/2018
ms.keywords: MI_CALLBACKMODE_INQUIRE, MI_CALLBACKMODE_REPORT, MI_OperationOptions_GetWriteErrorMode, MI_OperationOptions_GetWriteErrorMode function [Windows Management Infrastructure (MI)], mi/MI_OperationOptions_GetWriteErrorMode, wmi_v2.mi_operationoptions_getwriteerrormode
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
 - MI_OperationOptions_GetWriteErrorMode
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# MI_OperationOptions_GetWriteErrorMode function


## -description


Sets the error reporting mode.


## -parameters




### -param options [in]


<a href="https://msdn.microsoft.com/60445a53-c40c-4d0a-9650-21d0c7f3bbf6">MI_OperationOptions</a> structure.


### -param mode [out]

Returned MI_CallbackMode value.



#### MI_CALLBACKMODE_REPORT

Prompt will be passed back to the client in reporting mode, meaning the client is notified of the prompt but cannot respond to it and the server will automatically confirm the request.



#### MI_CALLBACKMODE_INQUIRE

Provider will block while the client is called back to ask if the operation should continue or not.


## -returns



A value of the <a href="https://msdn.microsoft.com/9AA2B479-E8A5-4F0C-A8A4-06DB7CB7CA2F">MI_Result</a> enumeration that specifies the function return code. This can be one of the following codes.



