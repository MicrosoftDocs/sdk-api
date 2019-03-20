---
UID: NF:mi.MI_DestinationOptions_SetString
title: MI_DestinationOptions_SetString function (mi.h)
author: windows-sdk-content
description: Sets a custom string option.
old-location: wmi_v2\mi_destinationoptions_setstring.htm
tech.root: wmi_v2
ms.assetid: 40621d0b-3ff2-4960-8cb0-e95bad0d08db
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: MI_DestinationOptions_SetString, MI_DestinationOptions_SetString function [Windows Management Infrastructure (MI)], mi/MI_DestinationOptions_SetString, wmi_v2.mi_destinationoptions_setstring
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
 - MI_DestinationOptions_SetString
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Management Framework 3.0 on Windows Server 2008 R2 with SP1, Windows 7 with SP1, and Windows Server 2008 with SP2
---

# MI_DestinationOptions_SetString function


## -description


Sets a custom string option.


## -parameters




### -param options [in, out]

A pointer to a <a href="https://msdn.microsoft.com/7f835ff4-3917-497c-bfe9-ca335cc35938">MI_DestinationOptions</a> object returned from the <a href="https://msdn.microsoft.com/efaa1244-7fe4-4484-b9ac-e7309e2012b6">MI_Application_NewDestinationOptions</a> function.


### -param optionName

A null-terminated string that represents the name of the option to set.


### -param optionValue

A null-terminated string that represents the new value of the option.


## -returns



A value of the <a href="https://msdn.microsoft.com/9AA2B479-E8A5-4F0C-A8A4-06DB7CB7CA2F">MI_Result</a> enumeration that specifies the function return code. This can be one of the following codes.




## -see-also




<a href="https://msdn.microsoft.com/efaa1244-7fe4-4484-b9ac-e7309e2012b6">MI_Application_NewDestinationOptions</a>



<a href="https://msdn.microsoft.com/7f835ff4-3917-497c-bfe9-ca335cc35938">MI_DestinationOptions</a>



<a href="https://msdn.microsoft.com/49bd7fa6-0164-4fb6-8154-75c39e6f7858">MI_DestinationOptions_GetString</a>
 

 

