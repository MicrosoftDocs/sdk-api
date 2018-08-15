---
UID: NF:mi.MI_Context_GetLocale
title: MI_Context_GetLocale function
author: windows-sdk-content
description: Retrieves the requested locale information that the client specified for the operation.
old-location: wmi_v2\mi_context_getlocale.htm
old-project: wmi_v2
ms.assetid: 7d2271e8-de76-4629-aedc-0ab882ab58eb
ms.author: windowssdkdev
ms.date: 08/03/2018
ms.keywords: MI_Context_GetLocale, MI_Context_GetLocale function [Windows Management Infrastructure (MI)], mi/MI_Context_GetLocale, wmi.mi_getlocale, wmi_v2.mi_context_getlocale
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: mi.h
req.include-header: 
req.redist: Windows Management Framework 3.0 on Windows Server 2008 R2 with SP1, Windows 7 with SP1, and Windows Server 2008 with SP2
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
 - MI_Context_GetLocale
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# MI_Context_GetLocale function


## -description


Retrieves the requested locale information that the client specified for the operation.


## -parameters




### -param context [in]

A pointer to the request context.


### -param localeType

The type of locale to be returned.


### -param locale

The returned locale.


## -returns



A value of the <a href="https://msdn.microsoft.com/9AA2B479-E8A5-4F0C-A8A4-06DB7CB7CA2F">MI_Result</a> enumeration that specifies the function return code. This can be one of the following codes.




## -remarks



There are two types of locale: UI and Data.  UI relates to the language of strings. Data relates to data formatting, such as date/time formats in strings and whether a decimal point or some other separator is used.



