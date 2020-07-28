---
UID: NF:mi.MI_OperationOptions_SetUseMachineID
title: MI_OperationOptions_SetUseMachineID function (mi.h)
description: Enables or disables the sending of machine identification information in the operation request.
helpviewer_keywords: ["MI_OperationOptions_SetUseMachineID","MI_OperationOptions_SetUseMachineID function [Windows Management Infrastructure (MI)]","mi/MI_OperationOptions_SetUseMachineID","wmi_v2.mi_operationoptions_setusemachineid"]
old-location: wmi_v2\mi_operationoptions_setusemachineid.htm
tech.root: wmi_v2
ms.assetid: 115fd37f-72e8-4a24-9362-5165b68ce257
ms.date: 12/05/2018
ms.keywords: MI_OperationOptions_SetUseMachineID, MI_OperationOptions_SetUseMachineID function [Windows Management Infrastructure (MI)], mi/MI_OperationOptions_SetUseMachineID, wmi_v2.mi_operationoptions_setusemachineid
f1_keywords:
- mi/MI_OperationOptions_SetUseMachineID
dev_langs:
- c++
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
- MI_OperationOptions_SetUseMachineID
targetos: Windows
req.typenames: 
req.redist: Windows Management Framework 3.0 on Windows Server 2008 R2 with SP1, Windows 7 with SP1, and Windows Server 2008 with SP2
ms.custom: 19H1
---

# MI_OperationOptions_SetUseMachineID function


## -description


Enables or disables the sending of machine identification information in the operation request.


## -parameters




### -param options [in, out]

A pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/mi/ns-mi-mi_operationoptions">MI_OperationOptions</a> structure.


### -param machineID [in]

Boolean value where <b>MI_TRUE</b> means to add the source machine name to the operation request packet so that the server can identify it. <b>MI_FALSE</b> means to not add the information.


## -returns



A value of the <a href="https://docs.microsoft.com/windows/desktop/api/mi/ne-mi-mi_result">MI_Result</a> enumeration that specifies the function return code. This can be one of the following codes.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mi/nf-mi-mi_operationoptions_getusemachineid">MI_OperationOptions_GetUseMachineID</a>
 

 

