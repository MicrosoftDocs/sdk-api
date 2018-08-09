---
UID: NF:mi.MI_Context_GetCustomOption
title: MI_Context_GetCustomOption function
author: windows-sdk-content
description: Retrieves an option set by the client.
old-location: wmi_v2\mi_context_getcustomoption.htm
old-project: wmi_v2
ms.assetid: 3338ca5c-48ac-450f-bf2a-ded6a2c3da19
ms.author: windowssdkdev
ms.date: 08/03/2018
ms.keywords: MI_Context_GetCustomOption, MI_Context_GetCustomOption function [Windows Management Infrastructure (MI)], mi/MI_Context_GetCustomOption, wmi.mi_getcustomoption, wmi_v2.mi_context_getcustomoption
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
 - MI_Context_GetCustomOption
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# MI_Context_GetCustomOption function


## -description


Retrieves an option set by the client.


## -parameters




### -param context [in]

A pointer to the request context.


### -param name

A pointer to the name of the option to get.


### -param valueType [out, optional]

A pointer to the option value type. This parameter is optional.


### -param value [out, optional]

A pointer to the option value. This parameter is optional.


## -returns



A value of the <a href="https://msdn.microsoft.com/9AA2B479-E8A5-4F0C-A8A4-06DB7CB7CA2F">MI_Result</a> enumeration that specifies the function return code. This can be one of the following codes.



