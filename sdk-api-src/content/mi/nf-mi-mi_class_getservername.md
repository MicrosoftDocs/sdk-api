---
UID: NF:mi.MI_Class_GetServerName
title: MI_Class_GetServerName function
author: windows-sdk-content
description: Gets the name of the server from the specified class.
old-location: wmi_v2\mi_class_getservername.htm
old-project: wmi_v2
ms.assetid: bb7312a0-f851-44a4-8467-31bbe1a9ac41
ms.author: windowssdkdev
ms.date: 06/14/2018
ms.keywords: MI_Class_GetServerName, MI_Class_GetServerName function [Windows Management Infrastructure (MI)], mi/MI_Class_GetServerName, wmi_v2.mi_class_getservername
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
 - MI_Class_GetServerName
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# MI_Class_GetServerName function


## -description


Gets the name of the server from the specified class.


## -parameters




### -param self [in]

A pointer to the class from which to retrieve the server name.


### -param serverName

A pointer to a pointer to the returned server name. This string is owned by the class and does not need to be deleted.


## -returns



This function returns MI_INLINE MI_Result.



