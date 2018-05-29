---
UID: NF:mi.MI_OperationOptions_GetTimeout
title: MI_OperationOptions_GetTimeout function
author: windows-sdk-content
description: Gets the operation timeout value.
old-location: wmi_v2\mi_operationoptions_gettimeout.htm
old-project: wmi_v2
ms.assetid: b55e75cc-86e5-4a4e-8bb7-2fec196033cc
ms.author: windowssdkdev
ms.date: 05/18/2018
ms.keywords: MI_OperationOptions_GetTimeout, MI_OperationOptions_GetTimeout function [Windows Management Infrastructure (MI)], mi/MI_OperationOptions_GetTimeout, wmi_v2.mi_operationoptions_gettimeout
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
req.typenames: MI_Type
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Mi.h
api_name:
-	MI_OperationOptions_GetTimeout
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# MI_OperationOptions_GetTimeout function


## -description


Gets the operation timeout value.


## -parameters




### -param options [in]


<a href="https://msdn.microsoft.com/60445a53-c40c-4d0a-9650-21d0c7f3bbf6">MI_OperationOptions</a> structure.


### -param timeout [out]

The operation's timeout value.


## -returns



A value of the <a href="https://msdn.microsoft.com/9AA2B479-E8A5-4F0C-A8A4-06DB7CB7CA2F">MI_Result</a> enumeration that specifies the function return code. This can be one of the following codes.




## -see-also




<a href="https://msdn.microsoft.com/73b640a4-db78-4cd2-af77-12317899d398">MI_OperationOptions_SetTimeout</a>
 

 

