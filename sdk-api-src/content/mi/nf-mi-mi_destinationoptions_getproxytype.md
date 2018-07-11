---
UID: NF:mi.MI_DestinationOptions_GetProxyType
title: MI_DestinationOptions_GetProxyType function
author: windows-sdk-content
description: Gets the proxy type set by the user.
old-location: wmi_v2\mi_destinationoptions_getproxytype.htm
old-project: wmi_v2
ms.assetid: d217940d-4531-4d3f-88c4-dc94e229af67
ms.author: windowssdkdev
ms.date: 06/14/2018
ms.keywords: MI_DESTINATIONOPTIONS_PROXY_TYPE_AUTO, MI_DESTINATIONOPTIONS_PROXY_TYPE_IE, MI_DESTINATIONOPTIONS_PROXY_TYPE_NONE, MI_DESTINATIONOPTIONS_PROXY_TYPE_WINHTTP, MI_DestinationOptions_GetProxyType, MI_DestinationOptions_GetProxyType function [Windows Management Infrastructure (MI)], mi/MI_DestinationOptions_GetProxyType, wmi_v2.mi_destinationoptions_getproxytype
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: MI_Type
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mi.h
api_name:
 - MI_DestinationOptions_GetProxyType
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# MI_DestinationOptions_GetProxyType function


## -description


Gets the proxy type set by the user.


## -parameters




### -param options [in]


<a href="https://msdn.microsoft.com/7f835ff4-3917-497c-bfe9-ca335cc35938">MI_DestinationOptions</a> object returned from <a href="https://msdn.microsoft.com/efaa1244-7fe4-4484-b9ac-e7309e2012b6">MI_Application_NewDestinationOptions</a>.


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



A value of the <a href="https://msdn.microsoft.com/9AA2B479-E8A5-4F0C-A8A4-06DB7CB7CA2F">MI_Result</a> enumeration that specifies the function return code. This can be one of the following codes.



