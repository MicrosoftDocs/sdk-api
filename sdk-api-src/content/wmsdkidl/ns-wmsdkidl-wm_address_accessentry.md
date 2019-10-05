---
UID: NS:wmsdkidl._WMAddressAccessEntry
title: WM_ADDRESS_ACCESSENTRY (wmsdkidl.h)
author: windows-sdk-content
description: The WM_ADDRESS_ACCESSENTRY structure specifies an entry in an IP address access list.
old-location: wmformat\wm_address_accessentry.htm
tech.root: wmformat
ms.assetid: 670c126f-c94b-4fac-b18c-d764f048f401
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: WM_ADDRESS_ACCESSENTRY, WM_ADDRESS_ACCESSENTRY structure [windows Media Format], wmformat.wm_address_accessentry, wmsdkidl/WM_ADDRESS_ACCESSENTRY
ms.topic: struct
f1_keywords: 
 - "wmsdkidl/WM_ADDRESS_ACCESSENTRY"
dev_langs:
 - c++
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
 - WM_ADDRESS_ACCESSENTRY
targetos: Windows
req.typenames: WM_ADDRESS_ACCESSENTRY
req.redist: 
ms.custom: 19H1
---

# WM_ADDRESS_ACCESSENTRY structure


## -description



The <b>WM_ADDRESS_ACCESSENTRY </b>structure specifies an entry in an IP address access list.




## -struct-fields




### -field dwIPAddress

An IPv4 address, in network byte order.


### -field dwMask

An IPv4 address, in network byte order, to use as a bitmask. The bitmask defines which bits in the <b>dwIPAddress</b> field are matched against. For example, if the IP address is 206.73.118.1 and the mask is 255.255.255.0, only the first 24 bits of the address are examined. Thus, any IP addresses in the range 206.73.118.<i>XXX</i> would match this entry.


## -remarks



You can use the <b>inet_addr</b> function to convert a standard dotted-format string (such as "255.255.255.255") to the correct binary number in network byte order.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmaddressaccess">IWMAddressAccess Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/wmformat/structures">Structures</a>
 

 

