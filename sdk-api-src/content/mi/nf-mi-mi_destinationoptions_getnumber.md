---
UID: NF:mi.MI_DestinationOptions_GetNumber
title: MI_DestinationOptions_GetNumber function
author: windows-sdk-content
description: Gets a previously added custom number option.
old-location: wmi_v2\mi_destinationoptions_getnumber.htm
tech.root: wmi_v2
ms.assetid: ac48c290-631f-427e-a544-ee0258029c42
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: MI_DestinationOptions_GetNumber, MI_DestinationOptions_GetNumber function [Windows Management Infrastructure (MI)], mi/MI_DestinationOptions_GetNumber, wmi_v2.mi_destinationoptions_getnumber
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
 - MI_DestinationOptions_GetNumber
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Management Framework 3.0 on Windows Server 2008 R2 with SP1, Windows 7 with SP1, and Windows Server 2008 with SP2
---

# MI_DestinationOptions_GetNumber function


## -description


Gets a previously added custom number option.


## -parameters




### -param options [in]


<a href="https://msdn.microsoft.com/7f835ff4-3917-497c-bfe9-ca335cc35938">MI_DestinationOptions</a> object returned from <a href="https://msdn.microsoft.com/efaa1244-7fe4-4484-b9ac-e7309e2012b6">MI_Application_NewDestinationOptions</a>.


### -param optionName

A null-terminated string that represents the name of the option to get.


### -param optionValue [out]

Returned option value.


### -param index [out, optional]

Returned zero-based index of the option.


## -returns



A value of the <a href="https://msdn.microsoft.com/9AA2B479-E8A5-4F0C-A8A4-06DB7CB7CA2F">MI_Result</a> enumeration that specifies the function return code. This can be one of the following codes.



