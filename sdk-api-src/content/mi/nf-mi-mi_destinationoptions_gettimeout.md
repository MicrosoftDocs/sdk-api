---
UID: NF:mi.MI_DestinationOptions_GetTimeout
title: MI_DestinationOptions_GetTimeout function (mi.h)
description: Gets the default options timeout value.
helpviewer_keywords: ["MI_DestinationOptions_GetTimeout","MI_DestinationOptions_GetTimeout function [Windows Management Infrastructure (MI)]","mi/MI_DestinationOptions_GetTimeout","wmi_v2.mi_destinationoptions_gettimeout"]
old-location: wmi_v2\mi_destinationoptions_gettimeout.htm
tech.root: wmi_v2
ms.assetid: e42765f1-42fd-49b2-ac70-bac42bd55441
ms.date: 12/05/2018
ms.keywords: MI_DestinationOptions_GetTimeout, MI_DestinationOptions_GetTimeout function [Windows Management Infrastructure (MI)], mi/MI_DestinationOptions_GetTimeout, wmi_v2.mi_destinationoptions_gettimeout
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
 - MI_DestinationOptions_GetTimeout
 - mi/MI_DestinationOptions_GetTimeout
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
 - MI_DestinationOptions_GetTimeout
---

# MI_DestinationOptions_GetTimeout function


## -description

Gets the default options timeout value.

## -parameters

### -param options [in]

<a href="/windows/desktop/api/mi/ns-mi-mi_destinationoptions">MI_DestinationOptions</a> object returned from <a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_application_newdestinationoptions">MI_Application_NewDestinationOptions</a>.

### -param timeout [out]

The returned timeout value.

## -returns

A value of the <a href="/windows/desktop/api/mi/ne-mi-mi_result">MI_Result</a> enumeration that specifies the function return code. This can be one of the following codes.

## -see-also

<a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_application_newdestinationoptions">MI_Application_NewDestinationOptions</a>



<a href="/windows/desktop/api/mi/ns-mi-mi_destinationoptions">MI_DestinationOptions</a>



<a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_destinationoptions_settimeout">MI_DestinationOptions_SetTimeout</a>



<a href="/windows/desktop/api/mi/ns-mi-mi_interval">MI_Interval</a>