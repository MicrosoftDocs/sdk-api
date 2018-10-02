---
UID: NF:mi.MI_Context_GetCustomOptionAt
title: MI_Context_GetCustomOptionAt function
author: windows-sdk-content
description: Retrieves an option at a particular index that was set by the client.
old-location: wmi_v2\mi_context_getcustomoptionat.htm
tech.root: WMI_v2
ms.assetid: f4f6c935-5207-46f6-b015-c4db724113f3
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: MI_Context_GetCustomOptionAt, MI_Context_GetCustomOptionAt function [Windows Management Infrastructure (MI)], mi/MI_Context_GetCustomOptionAt, wmi.mi_getcustomoptionat, wmi_v2.mi_context_getcustomoptionat
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
 - MI_Context_GetCustomOptionAt
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Management Framework 3.0 on Windows Server 2008 R2 with SP1, Windows 7 with SP1, and Windows Server 2008 with SP2
---

# MI_Context_GetCustomOptionAt function


## -description


Retrieves an option at a particular index that was set by the client.


## -parameters




### -param context [in]

A pointer to the request context.


### -param index [in]

The index of the option being retrieved. The index is zero based.


### -param name

A pointer to a pointer to the returned name or the retrieved option.


### -param valueType [out, optional]

A pointer to the returned option type. This parameter is optional.


### -param value [out, optional]

A pointer to the returned option value. This parameter is optional.


## -returns



A value of the <a href="https://msdn.microsoft.com/9AA2B479-E8A5-4F0C-A8A4-06DB7CB7CA2F">MI_Result</a> enumeration that specifies the function return code. This can be one of the following codes.




## -remarks



Note that the index used does not relate to the order in which the client may have created the options.



