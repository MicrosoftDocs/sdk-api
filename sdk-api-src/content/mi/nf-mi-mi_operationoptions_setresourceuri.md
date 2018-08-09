---
UID: NF:mi.MI_OperationOptions_SetResourceUri
title: MI_OperationOptions_SetResourceUri function
author: windows-sdk-content
description: Sets the resource URI to use for an operation.
old-location: wmi_v2\mi_operationoptions_setresourceuri.htm
old-project: wmi_v2
ms.assetid: 0722bc88-59a6-476b-a325-343d0eb43086
ms.author: windowssdkdev
ms.date: 08/03/2018
ms.keywords: MI_OperationOptions_SetResourceUri, MI_OperationOptions_SetResourceUri function [Windows Management Infrastructure (MI)], mi/MI_OperationOptions_SetResourceUri, wmi_v2.mi_operationoptions_setresourceuri
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
 - DllExport
api_location:
 - Mi.dll
api_name:
 - MI_OperationOptions_SetResourceUri
product: Windows
targetos: Windows
req.lib: Mi.lib
req.dll: Mi.dll
req.irql: 
req.product: GDI+ 1.1
---

# MI_OperationOptions_SetResourceUri function


## -description


Sets the resource URI to use for an operation.


## -parameters




### -param options [in, out]

A <a href="https://msdn.microsoft.com/60445a53-c40c-4d0a-9650-21d0c7f3bbf6">MI_OperationOptions</a> structure containing a set of operation options.


### -param rUri [in]

A null-terminated string that represents the resource URI to use for the operation.


## -returns



A value of the <a href="https://msdn.microsoft.com/9AA2B479-E8A5-4F0C-A8A4-06DB7CB7CA2F">MI_Result</a> enumeration that specifies the function return code. This can be one of the following codes.



