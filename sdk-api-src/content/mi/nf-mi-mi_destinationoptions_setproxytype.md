---
UID: NF:mi.MI_DestinationOptions_SetProxyType
title: MI_DestinationOptions_SetProxyType function (mi.h)
description: Sets the type of proxy settings to use when communicating to a destination through a proxy.
helpviewer_keywords: ["MI_DESTINATIONOPTIONS_PROXY_TYPE_AUTO","MI_DESTINATIONOPTIONS_PROXY_TYPE_IE","MI_DESTINATIONOPTIONS_PROXY_TYPE_NONE","MI_DESTINATIONOPTIONS_PROXY_TYPE_WINHTTP","MI_DestinationOptions_SetProxyType","MI_DestinationOptions_SetProxyType function [Windows Management Infrastructure (MI)]","mi/MI_DestinationOptions_SetProxyType","wmi_v2.mi_destinationoptions_setproxytype"]
old-location: wmi_v2\mi_destinationoptions_setproxytype.htm
tech.root: wmi_v2
ms.assetid: 6a4f9d1e-6885-497a-b931-1542af866f6b
ms.date: 12/05/2018
ms.keywords: MI_DESTINATIONOPTIONS_PROXY_TYPE_AUTO, MI_DESTINATIONOPTIONS_PROXY_TYPE_IE, MI_DESTINATIONOPTIONS_PROXY_TYPE_NONE, MI_DESTINATIONOPTIONS_PROXY_TYPE_WINHTTP, MI_DestinationOptions_SetProxyType, MI_DestinationOptions_SetProxyType function [Windows Management Infrastructure (MI)], mi/MI_DestinationOptions_SetProxyType, wmi_v2.mi_destinationoptions_setproxytype
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
 - MI_DestinationOptions_SetProxyType
 - mi/MI_DestinationOptions_SetProxyType
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
 - MI_DestinationOptions_SetProxyType
---

# MI_DestinationOptions_SetProxyType function


## -description

Sets the type of proxy settings to use when communicating to a destination through a proxy.

## -parameters

### -param options [in, out]

A pointer to a <a href="/windows/desktop/api/mi/ns-mi-mi_destinationoptions">MI_DestinationOptions</a> object returned from the <a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_application_newdestinationoptions">MI_Application_NewDestinationOptions</a> function.

### -param proxyType

A null-terminated string that represents the proxy mechanism to use. Possible values include these constants.



#### MI_DESTINATIONOPTIONS_PROXY_TYPE_IE ("IE")

Default IE settings.



#### MI_DESTINATIONOPTIONS_PROXY_TYPE_WINHTTP ("WinHTTP")

WinHTTP settings.



#### MI_DESTINATIONOPTIONS_PROXY_TYPE_AUTO ("Auto")

(Default setting) Provider selects the best option.



#### MI_DESTINATIONOPTIONS_PROXY_TYPE_NONE ("None")

Disables proxy usage.

## -remarks

Not all protocols and transports support proxy configurations.  The defaults for this setting will vary depending on the protocol and transport selected.

## -see-also

<a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_application_newdestinationoptions">MI_Application_NewDestinationOptions</a>



<a href="/windows/desktop/api/mi/ns-mi-mi_destinationoptions">MI_DestinationOptions</a>



<a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_destinationoptions_getproxytype">MI_DestinationOptions_GetProxyType</a>