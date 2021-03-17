---
UID: NF:mi.MI_DestinationOptions_SetHttpUrlPrefix
title: MI_DestinationOptions_SetHttpUrlPrefix function (mi.h)
description: Set the default HTTP URL prefix for transports that go over HTTP and HTTPS.
helpviewer_keywords: ["MI_DestinationOptions_SetHttpUrlPrefix","MI_DestinationOptions_SetHttpUrlPrefix function [Windows Management Infrastructure (MI)]","mi/MI_DestinationOptions_SetHttpUrlPrefix","wmi_v2.mi_destinationoptions_sethttpurlprefix"]
old-location: wmi_v2\mi_destinationoptions_sethttpurlprefix.htm
tech.root: wmi_v2
ms.assetid: fc5b6dd8-3243-49b4-a8da-8351a9c3f209
ms.date: 12/05/2018
ms.keywords: MI_DestinationOptions_SetHttpUrlPrefix, MI_DestinationOptions_SetHttpUrlPrefix function [Windows Management Infrastructure (MI)], mi/MI_DestinationOptions_SetHttpUrlPrefix, wmi_v2.mi_destinationoptions_sethttpurlprefix
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
 - MI_DestinationOptions_SetHttpUrlPrefix
 - mi/MI_DestinationOptions_SetHttpUrlPrefix
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
 - MI_DestinationOptions_SetHttpUrlPrefix
---

# MI_DestinationOptions_SetHttpUrlPrefix function


## -description

Set the default HTTP URL prefix for transports that go over HTTP and HTTPS.

## -parameters

### -param options [in, out]

A pointer to a <a href="/windows/desktop/api/mi/ns-mi-mi_destinationoptions">MI_DestinationOptions</a> object returned from the <a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_application_newdestinationoptions">MI_Application_NewDestinationOptions</a> function.

### -param prefix

A null-terminated string that represents the HTTP URL prefix ("HTTP" or "HTTPS").

## -returns

A value of the <a href="/windows/desktop/api/mi/ne-mi-mi_result">MI_Result</a> enumeration that specifies the function return code. This can be one of the following codes.

## -remarks

The default URL prefix is protocol specific.  This setting is ignored by transports that do not support this.

## -see-also

<a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_application_newdestinationoptions">MI_Application_NewDestinationOptions</a>



<a href="/windows/desktop/api/mi/ns-mi-mi_destinationoptions">MI_DestinationOptions</a>



<a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_destinationoptions_gethttpurlprefix">MI_DestinationOptions_GetHttpUrlPrefix</a>



<a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_destinationoptions_gettransport">MI_DestinationOptions_GetTransport</a>



<a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_destinationoptions_settransport">MI_DestinationOptions_SetTransport</a>