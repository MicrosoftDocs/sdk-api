---
UID: NF:mi.MI_DestinationOptions_SetTimeout
title: MI_DestinationOptions_SetTimeout function (mi.h)
description: Sets the default options timeout value.
helpviewer_keywords: ["MI_DestinationOptions_SetTimeout","MI_DestinationOptions_SetTimeout function [Windows Management Infrastructure (MI)]","mi/MI_DestinationOptions_SetTimeout","wmi_v2.mi_destinationoptions_settimeout"]
old-location: wmi_v2\mi_destinationoptions_settimeout.htm
tech.root: wmi_v2
ms.assetid: 81309b13-657c-45fc-b4fd-21bfb28247a2
ms.date: 12/05/2018
ms.keywords: MI_DestinationOptions_SetTimeout, MI_DestinationOptions_SetTimeout function [Windows Management Infrastructure (MI)], mi/MI_DestinationOptions_SetTimeout, wmi_v2.mi_destinationoptions_settimeout
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
targetos: Windows
req.typenames: 
req.redist: Windows Management Framework 3.0 on Windows Server 2008 R2 with SP1, Windows 7 with SP1, and Windows Server 2008 with SP2
ms.custom: 19H1
f1_keywords:
 - MI_DestinationOptions_SetTimeout
 - mi/MI_DestinationOptions_SetTimeout
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mi.h
api_name:
 - MI_DestinationOptions_SetTimeout
---

# MI_DestinationOptions_SetTimeout function


## -description

Sets the default options timeout value.

## -parameters

### -param options [in, out]

A pointer to a <a href="/windows/desktop/api/mi/ns-mi-mi_destinationoptions">MI_DestinationOptions</a> object returned from the <a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_application_newdestinationoptions">MI_Application_NewDestinationOptions</a> function.

### -param timeout [in]

A pointer to the new timeout value.

## -returns

A value of the <a href="/windows/desktop/api/mi/ne-mi-mi_result">MI_Result</a> enumeration that specifies the function return code. This can be one of the following codes.

## -remarks

If you need to run an operation that takes longer than usual, you can call the <a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_operationoptions_settimeout">MI_OperationOptions_SetTimeout</a> function to override the default timeout value.

## -see-also

<a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_application_newdestinationoptions">MI_Application_NewDestinationOptions</a>



<a href="/windows/desktop/api/mi/ns-mi-mi_destinationoptions">MI_DestinationOptions</a>



<a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_destinationoptions_gettimeout">MI_DestinationOptions_GetTimeout</a>



<a href="/windows/desktop/api/mi/ns-mi-mi_interval">MI_Interval</a>



<a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_operationoptions_settimeout">MI_OperationOptions_SetTimeout</a>