---
UID: NS:wmsdkidl._WMClientPropertiesEx
title: WM_CLIENT_PROPERTIES_EX (wmsdkidl.h)
author: windows-sdk-content
description: The WM_CLIENT_PROPERTIES_EX structure holds extended client information.
old-location: wmformat\wm_client_properties_ex.htm
tech.root: wmformat
ms.assetid: 981a466d-576b-4774-bd7b-785b0ef80e72
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: WM_CLIENT_PROPERTIES_EX, WM_CLIENT_PROPERTIES_EX structure [windows Media Format], wmformat.wm_client_properties_ex, wmsdkidl/WM_CLIENT_PROPERTIES_EX
ms.topic: struct
req.header: wmsdkidl.h
req.include-header: Wmsdk.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only],Windows Media Format 9 Series SDK, or later versions of the SDK
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wmsdkidl.h
api_name:
 - WM_CLIENT_PROPERTIES_EX
product: Windows
targetos: Windows
req.typenames: WM_CLIENT_PROPERTIES_EX
req.redist: 
---

# WM_CLIENT_PROPERTIES_EX structure


## -description



The <b>WM_CLIENT_PROPERTIES_EX </b>structure holds extended client information.




## -struct-fields




### -field cbSize

<b>DWORD</b> containing the size of the structure.


### -field pwszIPAddress

String containing the client's IP address in dot notation (for example, "192.168.10.2").


### -field pwszPort

String containing the client's port number.


### -field pwszDNSName

String containing the client's name on the domain name server (DNS), if known.


## -see-also




<a href="https://msdn.microsoft.com/118ef278-ca4f-4c30-9633-a2d851f5c758">Structures</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd757903(v=VS.85).aspx">WM_CLIENT_PROPERTIES</a>
 

 

