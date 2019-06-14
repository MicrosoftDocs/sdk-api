---
UID: NF:mi.MI_OperationOptions_GetTimeout
title: MI_OperationOptions_GetTimeout function (mi.h)
author: windows-sdk-content
description: Gets the operation timeout value.
old-location: wmi_v2\mi_operationoptions_gettimeout.htm
tech.root: wmi_v2
ms.assetid: b55e75cc-86e5-4a4e-8bb7-2fec196033cc
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: MI_OperationOptions_GetTimeout, MI_OperationOptions_GetTimeout function [Windows Management Infrastructure (MI)], mi/MI_OperationOptions_GetTimeout, wmi_v2.mi_operationoptions_gettimeout
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
 - MI_OperationOptions_GetTimeout
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Management Framework 3.0 on Windows Server 2008 R2 with SP1, Windows 7 with SP1, and Windows Server 2008 with SP2
ms.custom: 19H1
---

# MI_OperationOptions_GetTimeout function


## -description


Gets the operation timeout value.


## -parameters




### -param options [in]


<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mi/ns-mi-_mi_operationoptions">MI_OperationOptions</a> structure.


### -param timeout [out]

The operation's timeout value.


## -returns



A value of the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mi/ne-mi-_mi_result">MI_Result</a> enumeration that specifies the function return code. This can be one of the following codes.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mi/nf-mi-mi_operationoptions_settimeout">MI_OperationOptions_SetTimeout</a>
 

 

