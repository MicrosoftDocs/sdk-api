---
UID: NF:mi.MI_DestinationOptions_SetUILocale
title: MI_DestinationOptions_SetUILocale function
author: windows-sdk-content
description: Sets the default UI locale for operations.
old-location: wmi_v2\mi_destinationoptions_setuilocale.htm
tech.root: WMI_v2
ms.assetid: a536544c-003b-402e-9d63-d3e30b49cc39
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: MI_DestinationOptions_SetUILocale, MI_DestinationOptions_SetUILocale function [Windows Management Infrastructure (MI)], mi/MI_DestinationOptions_SetUILocale, wmi_v2.mi_destinationoptions_setuilocale
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
 - MI_DestinationOptions_SetUILocale
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Management Framework 3.0 on Windows Server 2008 R2 with SP1, Windows 7 with SP1, and Windows Server 2008 with SP2
- apiref
: 
- 
: 
- MI_DestinationOptions_SetUILocale
: 
---

# MI_DestinationOptions_SetUILocale function


## -description


Sets the default UI locale for operations.


## -parameters




### -param options [in, out]

A pointer to a <a href="https://msdn.microsoft.com/7f835ff4-3917-497c-bfe9-ca335cc35938">MI_DestinationOptions</a> object returned from the <a href="https://msdn.microsoft.com/efaa1244-7fe4-4484-b9ac-e7309e2012b6">MI_Application_NewDestinationOptions</a> function.


### -param locale

A null-terminated string that represents the locale string to be used (for example, "en-us").


## -returns



A value of the <a href="https://msdn.microsoft.com/9AA2B479-E8A5-4F0C-A8A4-06DB7CB7CA2F">MI_Result</a> enumeration that specifies the function return code. This can be one of the following codes.




## -remarks



The UI locale represents the language that error messages should come back to the client in.  By default, the UI locale of the calling thread for the execution of an operation would be used.




## -see-also




<a href="https://msdn.microsoft.com/efaa1244-7fe4-4484-b9ac-e7309e2012b6">MI_Application_NewDestinationOptions</a>



<a href="https://msdn.microsoft.com/7f835ff4-3917-497c-bfe9-ca335cc35938">MI_DestinationOptions</a>



<a href="https://msdn.microsoft.com/c05104c8-ecf7-447c-9cea-25a26b82bc69">MI_DestinationOptions_GetUILocale</a>
 

 

