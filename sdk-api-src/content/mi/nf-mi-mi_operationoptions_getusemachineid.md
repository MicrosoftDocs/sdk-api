---
UID: NF:mi.MI_OperationOptions_GetUseMachineID
title: MI_OperationOptions_GetUseMachineID function
author: windows-sdk-content
description: Gets the value that indicates whether to use machine identification information in the operation request.
old-location: wmi_v2\mi_operationoptions_getusemachineid.htm
tech.root: WMI_v2
ms.assetid: a3064be4-b975-47cb-b0f9-445a09791ebd
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: MI_OperationOptions_GetUseMachineID, MI_OperationOptions_GetUseMachineID function [Windows Management Infrastructure (MI)], mi/MI_OperationOptions_GetUseMachineID, wmi_v2.mi_operationoptions_getusemachineid
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
 - MI_OperationOptions_GetUseMachineID
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Management Framework 3.0 on Windows Server 2008 R2 with SP1, Windows 7 with SP1, and Windows Server 2008 with SP2
---

# MI_OperationOptions_GetUseMachineID function


## -description


Gets the value that indicates whether to use machine identification information in the operation request.


## -parameters




### -param options [in]


<a href="https://msdn.microsoft.com/60445a53-c40c-4d0a-9650-21d0c7f3bbf6">MI_OperationOptions</a> structure.


### -param machineID [out]

Returned Boolean value where <b>MI_TRUE</b> means that the source machine name is being added to the operation request packet so that the server can identify it. <b>MI_FALSE</b> means that the information is not being added.


## -returns



A value of the <a href="https://msdn.microsoft.com/9AA2B479-E8A5-4F0C-A8A4-06DB7CB7CA2F">MI_Result</a> enumeration that specifies the function return code. This can be one of the following codes.



