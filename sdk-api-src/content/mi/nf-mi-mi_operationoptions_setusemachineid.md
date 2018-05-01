---
UID: NF:mi.MI_OperationOptions_SetUseMachineID
title: MI_OperationOptions_SetUseMachineID function
author: windows-driver-content
description: Enables or disables the sending of machine identification information in the operation request.
old-location: wmi_v2\mi_operationoptions_setusemachineid.htm
old-project: wmi_v2
ms.assetid: 115fd37f-72e8-4a24-9362-5165b68ce257
ms.author: windowsdriverdev
ms.date: 4/18/2018
ms.keywords: MI_OperationOptions_SetUseMachineID, MI_OperationOptions_SetUseMachineID function [Windows Management Infrastructure (MI)], mi/MI_OperationOptions_SetUseMachineID, wmi_v2.mi_operationoptions_setusemachineid
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
req.typenames: MI_Type
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Mi.h
api_name:
-	MI_OperationOptions_SetUseMachineID
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# MI_OperationOptions_SetUseMachineID function


## -description


Enables or disables the sending of machine identification information in the operation request.


## -parameters




### -param options [in, out]

A pointer to a <a href="https://msdn.microsoft.com/60445a53-c40c-4d0a-9650-21d0c7f3bbf6">MI_OperationOptions</a> structure.


### -param machineID [in]

Boolean value where <b>MI_TRUE</b> means to add the source machine name to the operation request packet so that the server can identify it. <b>MI_FALSE</b> means to not add the information.


## -returns



A value of the <a href="https://msdn.microsoft.com/9AA2B479-E8A5-4F0C-A8A4-06DB7CB7CA2F">MI_Result</a> enumeration that specifies the function return code. This can be one of the following codes.




## -see-also




<a href="https://msdn.microsoft.com/a3064be4-b975-47cb-b0f9-445a09791ebd">MI_OperationOptions_GetUseMachineID</a>
 

 

