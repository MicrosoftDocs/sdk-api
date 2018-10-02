---
UID: NF:mi.MI_DestinationOptions_GetDataLocale
title: MI_DestinationOptions_GetDataLocale function
author: windows-sdk-content
description: Gets the data locale (as opposed to UI locale) set by the user.
old-location: wmi_v2\mi_destinationoptions_getdatalocale.htm
tech.root: WMI_v2
ms.assetid: 301cf7d1-0df3-43e6-940d-4c0f29c8cd76
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: MI_DestinationOptions_GetDataLocale, MI_DestinationOptions_GetDataLocale function [Windows Management Infrastructure (MI)], mi/MI_DestinationOptions_GetDataLocale, wmi_v2.mi_destinationoptions_getdatalocale
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
 - MI_DestinationOptions_GetDataLocale
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Management Framework 3.0 on Windows Server 2008 R2 with SP1, Windows 7 with SP1, and Windows Server 2008 with SP2
---

# MI_DestinationOptions_GetDataLocale function


## -description


Gets the data locale (as opposed to UI locale) set by the user.


## -parameters




### -param options [in]


<a href="https://msdn.microsoft.com/7f835ff4-3917-497c-bfe9-ca335cc35938">MI_DestinationOptions</a> object returned from <a href="https://msdn.microsoft.com/efaa1244-7fe4-4484-b9ac-e7309e2012b6">MI_Application_NewDestinationOptions</a>.


### -param locale

A pointer to a null-terminated string containing the returned data locale. The memory is owned by the destination options object, so it does not need to be deleted.


## -returns



A value of the <a href="https://msdn.microsoft.com/9AA2B479-E8A5-4F0C-A8A4-06DB7CB7CA2F">MI_Result</a> enumeration that specifies the function return code. This can be one of the following codes.




## -remarks



The data locale determines string formats for entities such as decimal numbers in string format and date/time formats.



