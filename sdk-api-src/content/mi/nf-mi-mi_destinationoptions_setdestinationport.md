---
UID: NF:mi.MI_DestinationOptions_SetDestinationPort
title: MI_DestinationOptions_SetDestinationPort function (mi.h)
description: Set the port to use to communicate to the destination.
helpviewer_keywords: ["MI_DestinationOptions_SetDestinationPort","MI_DestinationOptions_SetDestinationPort function [Windows Management Infrastructure (MI)]","mi/MI_DestinationOptions_SetDestinationPort","wmi_v2.mi_destinationoptions_setdestinationport"]
old-location: wmi_v2\mi_destinationoptions_setdestinationport.htm
tech.root: wmi_v2
ms.assetid: 4359eb04-aaf7-490f-ab60-b42182b53611
ms.date: 12/05/2018
ms.keywords: MI_DestinationOptions_SetDestinationPort, MI_DestinationOptions_SetDestinationPort function [Windows Management Infrastructure (MI)], mi/MI_DestinationOptions_SetDestinationPort, wmi_v2.mi_destinationoptions_setdestinationport
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
 - MI_DestinationOptions_SetDestinationPort
 - mi/MI_DestinationOptions_SetDestinationPort
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
 - MI_DestinationOptions_SetDestinationPort
---

# MI_DestinationOptions_SetDestinationPort function


## -description

Set the port to use to communicate to the destination.

## -parameters

### -param options [in, out]

A pointer to a <a href="/windows/desktop/api/mi/ns-mi-mi_destinationoptions">MI_DestinationOptions</a> object returned from the <a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_application_newdestinationoptions">MI_Application_NewDestinationOptions</a> function.

### -param port

Transport port used to communicate with the server.

## -returns

A value of the <a href="/windows/desktop/api/mi/ne-mi-mi_result">MI_Result</a> enumeration that specifies the function return code. This can be one of the following codes.

## -remarks

Not all transports and protocols will allow the port to be changed, in which case setting this option will be ignored.  The default port used is transport-specific.

## -see-also

<a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_application_newdestinationoptions">MI_Application_NewDestinationOptions</a>



<a href="/windows/desktop/api/mi/ns-mi-mi_destinationoptions">MI_DestinationOptions</a>



<a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_destinationoptions_getdestinationport">MI_DestinationOptions_GetDestinationPort</a>