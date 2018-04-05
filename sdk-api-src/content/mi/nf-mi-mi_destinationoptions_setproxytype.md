---
UID: NF:mi.MI_DestinationOptions_SetProxyType
title: MI_DestinationOptions_SetProxyType function
author: windows-driver-content
description: Sets the type of proxy settings to use when communicating to a destination through a proxy.
old-location: wmi_v2\mi_destinationoptions_setproxytype.htm
old-project: wmi_v2
ms.assetid: 6a4f9d1e-6885-497a-b931-1542af866f6b
ms.author: windowsdriverdev
ms.date: 3/23/2018
ms.keywords: MI_DESTINATIONOPTIONS_PROXY_TYPE_AUTO, MI_DESTINATIONOPTIONS_PROXY_TYPE_IE, MI_DESTINATIONOPTIONS_PROXY_TYPE_NONE, MI_DESTINATIONOPTIONS_PROXY_TYPE_WINHTTP, MI_DestinationOptions_SetProxyType, MI_DestinationOptions_SetProxyType function [Windows Management Infrastructure (MI)], mi/MI_DestinationOptions_SetProxyType, wmi_v2.mi_destinationoptions_setproxytype
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: MI_Type
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Mi.h
api_name:
-	MI_DestinationOptions_SetProxyType
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# MI_DestinationOptions_SetProxyType function


## -description


Sets the type of proxy settings to use when communicating to a destination through a proxy.


## -parameters




### -param options [in, out]

A pointer to a <a href="https://msdn.microsoft.com/7f835ff4-3917-497c-bfe9-ca335cc35938">MI_DestinationOptions</a> object returned from the <a href="https://msdn.microsoft.com/efaa1244-7fe4-4484-b9ac-e7309e2012b6">MI_Application_NewDestinationOptions</a> function.


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




<a href="https://msdn.microsoft.com/efaa1244-7fe4-4484-b9ac-e7309e2012b6">MI_Application_NewDestinationOptions</a>



<a href="https://msdn.microsoft.com/7f835ff4-3917-497c-bfe9-ca335cc35938">MI_DestinationOptions</a>



<a href="https://msdn.microsoft.com/d217940d-4531-4d3f-88c4-dc94e229af67">MI_DestinationOptions_GetProxyType</a>
 

 

