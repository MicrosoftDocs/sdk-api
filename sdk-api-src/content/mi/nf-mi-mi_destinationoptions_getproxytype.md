---
UID: NF:mi.MI_DestinationOptions_GetProxyType
title: MI_DestinationOptions_GetProxyType function (mi.h)
description: Gets the proxy type set by the user.
helpviewer_keywords: ["MI_DESTINATIONOPTIONS_PROXY_TYPE_AUTO","MI_DESTINATIONOPTIONS_PROXY_TYPE_IE","MI_DESTINATIONOPTIONS_PROXY_TYPE_NONE","MI_DESTINATIONOPTIONS_PROXY_TYPE_WINHTTP","MI_DestinationOptions_GetProxyType","MI_DestinationOptions_GetProxyType function [Windows Management Infrastructure (MI)]","mi/MI_DestinationOptions_GetProxyType","wmi_v2.mi_destinationoptions_getproxytype"]
old-location: wmi_v2\mi_destinationoptions_getproxytype.htm
tech.root: wmi_v2
ms.assetid: d217940d-4531-4d3f-88c4-dc94e229af67
ms.date: 12/05/2018
ms.keywords: MI_DESTINATIONOPTIONS_PROXY_TYPE_AUTO, MI_DESTINATIONOPTIONS_PROXY_TYPE_IE, MI_DESTINATIONOPTIONS_PROXY_TYPE_NONE, MI_DESTINATIONOPTIONS_PROXY_TYPE_WINHTTP, MI_DestinationOptions_GetProxyType, MI_DestinationOptions_GetProxyType function [Windows Management Infrastructure (MI)], mi/MI_DestinationOptions_GetProxyType, wmi_v2.mi_destinationoptions_getproxytype
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
 - MI_DestinationOptions_GetProxyType
 - mi/MI_DestinationOptions_GetProxyType
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
 - MI_DestinationOptions_GetProxyType
---

# MI_DestinationOptions_GetProxyType function


## -description

Gets the proxy type set by the user.

## -parameters

### -param options [in]

<a href="/windows/desktop/api/mi/ns-mi-mi_destinationoptions">MI_DestinationOptions</a> object returned from <a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_application_newdestinationoptions">MI_Application_NewDestinationOptions</a>.

### -param proxyType

A pointer to a null-terminated string containing the returned proxy type. This string can be one of these values:



#### MI_DESTINATIONOPTIONS_PROXY_TYPE_IE ("IE")

Default IE settings.



#### MI_DESTINATIONOPTIONS_PROXY_TYPE_WINHTTP ("WinHTTP")

WinHTTP settings.



#### MI_DESTINATIONOPTIONS_PROXY_TYPE_AUTO ("Auto")

(Default setting) Provider selects the best option.



#### MI_DESTINATIONOPTIONS_PROXY_TYPE_NONE ("None")

Disables proxy usage.

## -returns

A value of the <a href="/windows/desktop/api/mi/ne-mi-mi_result">MI_Result</a> enumeration that specifies the function return code. This can be one of the following codes.