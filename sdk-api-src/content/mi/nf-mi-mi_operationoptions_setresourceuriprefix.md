---
UID: NF:mi.MI_OperationOptions_SetResourceUriPrefix
title: MI_OperationOptions_SetResourceUriPrefix function
author: windows-sdk-content
description: Sets the resource URI prefix to use for an operation.
old-location: wmi_v2\mi_operationoptions_setresourceuriprefix.htm
old-project: wmi_v2
ms.assetid: 7f384720-7673-4dd2-883f-a52da4a51729
ms.author: windowssdkdev
ms.date: 06/14/2018
ms.keywords: MI_OperationOptions_SetResourceUriPrefix, MI_OperationOptions_SetResourceUriPrefix function [Windows Management Infrastructure (MI)], mi/MI_OperationOptions_SetResourceUriPrefix, wmi_v2.mi_operationoptions_setresourceuriprefix
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
 - MI_OperationOptions_SetResourceUriPrefix
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# MI_OperationOptions_SetResourceUriPrefix function


## -description


Sets the resource URI prefix to use for an operation.


## -parameters




### -param options [in, out]

A pointer to a <a href="https://msdn.microsoft.com/60445a53-c40c-4d0a-9650-21d0c7f3bbf6">MI_OperationOptions</a> structure.


### -param ruriPrefix

A null-terminated string that represents the resource URI to use for the operation.


## -returns



A value of the <a href="https://msdn.microsoft.com/9AA2B479-E8A5-4F0C-A8A4-06DB7CB7CA2F">MI_Result</a> enumeration that specifies the function return code. This can be one of the following codes.




## -see-also




<a href="https://msdn.microsoft.com/c6ef1e8c-0d80-4359-a0f4-9d25ed39eae3">MI_OperationOptions_GetResourceUriPrefix</a>
 

 

