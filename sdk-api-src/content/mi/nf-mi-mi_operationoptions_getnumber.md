---
UID: NF:mi.MI_OperationOptions_GetNumber
title: MI_OperationOptions_GetNumber function
author: windows-sdk-content
description: Gets a previously added custom number option.
old-location: wmi_v2\mi_operationoptions_getnumber.htm
tech.root: WMI_v2
ms.assetid: 5c22c18d-9e1f-4cf7-84c1-e4e8863d0dc1
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: MI_OperationOptions_GetNumber, MI_OperationOptions_GetNumber function [Windows Management Infrastructure (MI)], mi/MI_OperationOptions_GetNumber, wmi_v2.mi_operationoptions_getnumber
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
 - MI_OperationOptions_GetNumber
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Management Framework 3.0 on Windows Server 2008 R2 with SP1, Windows 7 with SP1, and Windows Server 2008 with SP2
- apiref
: 
- 
: 
- MI_OperationOptions_GetNumber
: 
---

# MI_OperationOptions_GetNumber function


## -description


Gets a previously added custom number option.


## -parameters




### -param options [in]


<a href="https://msdn.microsoft.com/60445a53-c40c-4d0a-9650-21d0c7f3bbf6">MI_OperationOptions</a> structure.


### -param optionName

A null-terminated string that represents the name of the option to get.


### -param value [out]

Returned option value.


### -param index [out, optional]

Returned zero-based index of the option.


### -param flags [out, optional]

Returned option flags.


## -returns



A value of the <a href="https://msdn.microsoft.com/9AA2B479-E8A5-4F0C-A8A4-06DB7CB7CA2F">MI_Result</a> enumeration that specifies the function return code. This can be one of the following codes.



