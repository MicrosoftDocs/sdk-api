---
UID: NF:mi.MI_DestinationOptions_GetOption
title: MI_DestinationOptions_GetOption function
author: windows-sdk-content
description: Gets a previously added option value based on the option name.
old-location: wmi_v2\mi_destinationoptions_getoption.htm
old-project: wmi_v2
ms.assetid: f7f26a4f-109f-4169-bc77-b0c763d7bcb8
ms.author: windowssdkdev
ms.date: 05/18/2018
ms.keywords: MI_DestinationOptions_GetOption, MI_DestinationOptions_GetOption function [Windows Management Infrastructure (MI)], mi/MI_DestinationOptions_GetOption, wmi_v2.mi_destinationoptions_getoption
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
 - MI_DestinationOptions_GetOption
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# MI_DestinationOptions_GetOption function


## -description


Gets a previously added option value based on the option name.


## -parameters




### -param options [in]


<a href="https://msdn.microsoft.com/7f835ff4-3917-497c-bfe9-ca335cc35938">MI_DestinationOptions</a> object returned from <a href="https://msdn.microsoft.com/efaa1244-7fe4-4484-b9ac-e7309e2012b6">MI_Application_NewDestinationOptions</a>.


### -param optionName

A null-terminated string that represents the name of the option to get.


### -param value [out]

The returned option value. This value is owned by the destination options object, so there is no need to delete it.


### -param type [out]

Returned option type.


### -param index [out, optional]

Returned zero-based index of the option.


### -param flags [out, optional]

Returned option flags.


## -returns



A value of the <a href="https://msdn.microsoft.com/9AA2B479-E8A5-4F0C-A8A4-06DB7CB7CA2F">MI_Result</a> enumeration that specifies the function return code. This can be one of the following codes.



