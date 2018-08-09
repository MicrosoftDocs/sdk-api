---
UID: NF:mi.MI_DestinationOptions_SetNumber
title: MI_DestinationOptions_SetNumber function
author: windows-sdk-content
description: Sets a custom numeric option value.
old-location: wmi_v2\mi_destinationoptions_setnumber.htm
old-project: wmi_v2
ms.assetid: 46e81ecd-7fb5-465a-8caa-04288c559fea
ms.author: windowssdkdev
ms.date: 08/03/2018
ms.keywords: MI_DestinationOptions_SetNumber, MI_DestinationOptions_SetNumber function [Windows Management Infrastructure (MI)], mi/MI_DestinationOptions_SetNumber, wmi_v2.mi_destinationoptions_setnumber
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
 - MI_DestinationOptions_SetNumber
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# MI_DestinationOptions_SetNumber function


## -description


Sets a custom numeric option value.


## -parameters




### -param options [in, out]

A pointer to a <a href="https://msdn.microsoft.com/7f835ff4-3917-497c-bfe9-ca335cc35938">MI_DestinationOptions</a> object returned from the <a href="https://msdn.microsoft.com/efaa1244-7fe4-4484-b9ac-e7309e2012b6">MI_Application_NewDestinationOptions</a> function.


### -param optionName

A null-terminated string that represents the name of option to set.


### -param optionValue [in]

New option value.


## -returns



A value of the <a href="https://msdn.microsoft.com/9AA2B479-E8A5-4F0C-A8A4-06DB7CB7CA2F">MI_Result</a> enumeration that specifies the function return code. This can be one of the following codes.




## -see-also




<a href="https://msdn.microsoft.com/efaa1244-7fe4-4484-b9ac-e7309e2012b6">MI_Application_NewDestinationOptions</a>



<a href="https://msdn.microsoft.com/7f835ff4-3917-497c-bfe9-ca335cc35938">MI_DestinationOptions</a>



<a href="https://msdn.microsoft.com/ac48c290-631f-427e-a544-ee0258029c42">MI_DestinationOptions_GetNumber</a>
 

 

