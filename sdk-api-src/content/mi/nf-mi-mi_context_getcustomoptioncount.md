---
UID: NF:mi.MI_Context_GetCustomOptionCount
title: MI_Context_GetCustomOptionCount function
author: windows-driver-content
description: Gets the number of custom options available to the provider.
old-location: wmi_v2\mi_context_getcustomoptioncount.htm
old-project: wmi_v2
ms.assetid: 8cce1492-5c3a-4ba8-8f33-22f6ff7fcf3a
ms.author: windowsdriverdev
ms.date: 4/18/2018
ms.keywords: MI_Context_GetCustomOptionCount, MI_Context_GetCustomOptionCount function [Windows Management Infrastructure (MI)], mi/MI_Context_GetCustomOptionCount, wmi.mi_getcustomoptioncount, wmi_v2.mi_context_getcustomoptioncount
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
-	MI_Context_GetCustomOptionCount
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# MI_Context_GetCustomOptionCount function


## -description


Gets the number of custom options available to the provider.


## -parameters




### -param context [in]

A pointer to the request context.


### -param count [out, optional]

A pointer to the returned number of options. This parameter is optional.


## -returns



A value of the <a href="https://msdn.microsoft.com/9AA2B479-E8A5-4F0C-A8A4-06DB7CB7CA2F">MI_Result</a> enumeration that specifies the function return code. This can be one of the following codes.




## -remarks



These options are passed by the client, possibly through the <a href="https://msdn.microsoft.com/60445a53-c40c-4d0a-9650-21d0c7f3bbf6">MI_OperationOptions</a> structure.




## -see-also




<a href="https://msdn.microsoft.com/60445a53-c40c-4d0a-9650-21d0c7f3bbf6">MI_OperationOptions</a>
 

 

