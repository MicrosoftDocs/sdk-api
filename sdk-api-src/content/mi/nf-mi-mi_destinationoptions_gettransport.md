---
UID: NF:mi.MI_DestinationOptions_GetTransport
title: MI_DestinationOptions_GetTransport function (mi.h)
description: Gets the transport setting that the client added.
helpviewer_keywords: ["MI_DestinationOptions_GetTransport","MI_DestinationOptions_GetTransport function [Windows Management Infrastructure (MI)]","mi/MI_DestinationOptions_GetTransport","wmi_v2.mi_destinationoptions_gettransport"]
old-location: wmi_v2\mi_destinationoptions_gettransport.htm
tech.root: wmi_v2
ms.assetid: 85e0a952-c51c-4877-b9fb-d2fe0d0b1bb1
ms.date: 12/05/2018
ms.keywords: MI_DestinationOptions_GetTransport, MI_DestinationOptions_GetTransport function [Windows Management Infrastructure (MI)], mi/MI_DestinationOptions_GetTransport, wmi_v2.mi_destinationoptions_gettransport
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
 - MI_DestinationOptions_GetTransport
 - mi/MI_DestinationOptions_GetTransport
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
 - MI_DestinationOptions_GetTransport
---

# MI_DestinationOptions_GetTransport function


## -description

Gets the transport setting that the client added.

## -parameters

### -param options [in]

<a href="/windows/desktop/api/mi/ns-mi-mi_destinationoptions">MI_DestinationOptions</a> object returned from <a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_application_newdestinationoptions">MI_Application_NewDestinationOptions</a>.

### -param transport

A pointer to a null-terminated string that represents the returned transport setting. Supported transport setting values are listed in the <a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_destinationoptions_settransport">MI_DestinationOptions_SetTransport</a> function summary.

## -returns

A value of the <a href="/windows/desktop/api/mi/ne-mi-mi_result">MI_Result</a> enumeration that specifies the function return code. This can be one of the following codes.

## -see-also

<a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_application_newdestinationoptions">MI_Application_NewDestinationOptions</a>



<a href="/windows/desktop/api/mi/ns-mi-mi_destinationoptions">MI_DestinationOptions</a>



<a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_destinationoptions_settransport">MI_DestinationOptions_SetTransport</a>