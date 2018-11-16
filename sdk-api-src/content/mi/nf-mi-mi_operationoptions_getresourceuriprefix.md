---
UID: NF:mi.MI_OperationOptions_GetResourceUriPrefix
title: MI_OperationOptions_GetResourceUriPrefix function
author: windows-sdk-content
description: Gets the resource URI prefix being used for an operation.
old-location: wmi_v2\mi_operationoptions_getresourceuriprefix.htm
tech.root: wmi_v2
ms.assetid: c6ef1e8c-0d80-4359-a0f4-9d25ed39eae3
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: MI_OperationOptions_GetResourceUriPrefix, MI_OperationOptions_GetResourceUriPrefix function [Windows Management Infrastructure (MI)], mi/MI_OperationOptions_GetResourceUriPrefix, wmi_v2.mi_operationoptions_getresourceuriprefix
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mi.h
api_name:
 - MI_OperationOptions_GetResourceUriPrefix
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Management Framework 3.0 on Windows Server 2008 R2 with SP1, Windows 7 with SP1, and Windows Server 2008 with SP2
- apiref
: 
- 
: 
- MI_OperationOptions_GetResourceUriPrefix
: 
---

# MI_OperationOptions_GetResourceUriPrefix function


## -description


Gets the resource URI prefix being used for an operation.


## -parameters




### -param options [in]


<a href="https://msdn.microsoft.com/60445a53-c40c-4d0a-9650-21d0c7f3bbf6">MI_OperationOptions</a> structure.


### -param ruriPrefix

Returned resource URI being used for the operation.


## -returns



A value of the <a href="https://msdn.microsoft.com/9AA2B479-E8A5-4F0C-A8A4-06DB7CB7CA2F">MI_Result</a> enumeration that specifies the function return code. This can be one of the following codes.



