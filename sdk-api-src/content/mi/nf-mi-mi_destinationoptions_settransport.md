---
UID: NF:mi.MI_DestinationOptions_SetTransport
title: MI_DestinationOptions_SetTransport function (mi.h)
description: Sets the transport to be used to communicate with the destination machine.
helpviewer_keywords: ["MI_DESTINATIONOPTIONS_TRANPSORT_HTTPS","MI_DESTINATIONOPTIONS_TRANSPORT_HTTP","MI_DestinationOptions_SetTransport","MI_DestinationOptions_SetTransport function [Windows Management Infrastructure (MI)]","mi/MI_DestinationOptions_SetTransport","wmi_v2.mi_destinationoptions_settransport"]
old-location: wmi_v2\mi_destinationoptions_settransport.htm
tech.root: wmi_v2
ms.assetid: 998ac6ee-29a4-49bf-8ca1-01b7afddd33f
ms.date: 12/05/2018
ms.keywords: MI_DESTINATIONOPTIONS_TRANPSORT_HTTPS, MI_DESTINATIONOPTIONS_TRANSPORT_HTTP, MI_DestinationOptions_SetTransport, MI_DestinationOptions_SetTransport function [Windows Management Infrastructure (MI)], mi/MI_DestinationOptions_SetTransport, wmi_v2.mi_destinationoptions_settransport
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
 - MI_DestinationOptions_SetTransport
 - mi/MI_DestinationOptions_SetTransport
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
 - MI_DestinationOptions_SetTransport
---

# MI_DestinationOptions_SetTransport function


## -description

Sets the transport to be used to communicate with the destination machine.

## -parameters

### -param options [in, out]

A pointer to a <a href="/windows/desktop/api/mi/ns-mi-mi_destinationoptions">MI_DestinationOptions</a> object returned from the <a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_application_newdestinationoptions">MI_Application_NewDestinationOptions</a> function.

### -param transport

A null-terminated string that represents the transport setting. The value can be any of these constants.



#### MI_DESTINATIONOPTIONS_TRANSPORT_HTTP ("HTTP")

HTTP protocol. Even with HTTP, some authentication schemes allow the payload to be encrypted using the authentication token. Some examples of this include Kerberos, Negotiate, and CredSSP. However, HTTP headers will still be in plain text.



#### MI_DESTINATIONOPTIONS_TRANPSORT_HTTPS ("HTTPS")

HTTPS protocol where the channel is encrypted. Note the misspelling of "TRANPSORT".

## -returns

A value of the <a href="/windows/desktop/api/mi/ne-mi-mi_result">MI_Result</a> enumeration that specifies the function return code. This can be one of the following codes.

## -remarks

Not all protocols allow different underlying transports to be selected. If not supported, this setting will be ignored.

## -see-also

<a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_application_newdestinationoptions">MI_Application_NewDestinationOptions</a>



<a href="/windows/desktop/api/mi/ns-mi-mi_destinationoptions">MI_DestinationOptions</a>



<a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_destinationoptions_gettransport">MI_DestinationOptions_GetTransport</a>