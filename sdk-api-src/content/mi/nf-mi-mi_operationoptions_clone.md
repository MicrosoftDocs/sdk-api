---
UID: NF:mi.MI_OperationOptions_Clone
title: MI_OperationOptions_Clone function
author: windows-sdk-content
description: Creates a copy of a MI_OperationOptions structure.
old-location: wmi_v2\mi_operationoptions_clone.htm
tech.root: wmi_v2
ms.assetid: 22cce14f-55f0-4d31-a6cf-ea5e0a733d68
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: MI_OperationOptions_Clone, MI_OperationOptions_Clone function [Windows Management Infrastructure (MI)], mi/MI_OperationOptions_Clone, wmi_v2.mi_operationoptions_clone
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
 - MI_OperationOptions_Clone
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Management Framework 3.0 on Windows Server 2008 R2 with SP1, Windows 7 with SP1, and Windows Server 2008 with SP2
---

# MI_OperationOptions_Clone function


## -description


Creates a copy of a <a href="https://msdn.microsoft.com/60445a53-c40c-4d0a-9650-21d0c7f3bbf6">MI_OperationOptions</a> structure.


## -parameters




### -param self [in]


<a href="https://msdn.microsoft.com/60445a53-c40c-4d0a-9650-21d0c7f3bbf6">MI_OperationOptions</a> structure to be cloned.


### -param newOperationOptions [out]

Returned <a href="https://msdn.microsoft.com/60445a53-c40c-4d0a-9650-21d0c7f3bbf6">MI_OperationOptions</a> clone. When it is no longer needed, the clone needs to be deleted using the <a href="https://msdn.microsoft.com/a9e43835-92a4-468a-9d45-1d4ab81d94f0">MI_OperationOptions_Delete</a> function.


## -returns



This function returns MI_INLINE MI_Result MI_INLINE_CALL.




## -see-also




<a href="https://msdn.microsoft.com/a9e43835-92a4-468a-9d45-1d4ab81d94f0">MI_OperationOptions_Delete</a>
 

 

