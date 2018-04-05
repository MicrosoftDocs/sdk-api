---
UID: NF:mi.MI_OperationOptions_GetOptionCount
title: MI_OperationOptions_GetOptionCount function
author: windows-driver-content
description: Gets the number of options previously added.
old-location: wmi_v2\mi_operationoptions_getoptioncount.htm
old-project: wmi_v2
ms.assetid: 0c015ec7-d663-4207-b6d0-149da41cbf0e
ms.author: windowsdriverdev
ms.date: 3/23/2018
ms.keywords: MI_OperationOptions_GetOptionCount, MI_OperationOptions_GetOptionCount function [Windows Management Infrastructure (MI)], mi/MI_OperationOptions_GetOptionCount, wmi_v2.mi_operationoptions_getoptioncount
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
-	MI_OperationOptions_GetOptionCount
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# MI_OperationOptions_GetOptionCount function


## -description


Gets the number of options previously added.


## -parameters




### -param options [in]


<a href="https://msdn.microsoft.com/60445a53-c40c-4d0a-9650-21d0c7f3bbf6">MI_OperationOptions</a> structure.


### -param count [out]

Returned number of options.


## -returns



A value of the <a href="https://msdn.microsoft.com/9AA2B479-E8A5-4F0C-A8A4-06DB7CB7CA2F">MI_Result</a> enumeration that specifies the function return code. This can be one of the following codes.



