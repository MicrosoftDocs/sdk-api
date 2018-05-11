---
UID: NS:wmsdkidl._WMAddressAccessEntry
title: "_WMAddressAccessEntry"
author: windows-driver-content
description: The WM_ADDRESS_ACCESSENTRY structure specifies an entry in an IP address access list.
old-location: wmformat\wm_address_accessentry.htm
old-project: wmformat
ms.assetid: 670c126f-c94b-4fac-b18c-d764f048f401
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: WM_ADDRESS_ACCESSENTRY, WM_ADDRESS_ACCESSENTRY structure [windows Media Format], _WMAddressAccessEntry, wmformat.wm_address_accessentry, wmsdkidl/WM_ADDRESS_ACCESSENTRY
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: WM_ADDRESS_ACCESSENTRY
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Wmsdkidl.h
api_name:
-	WM_ADDRESS_ACCESSENTRY
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# _WMAddressAccessEntry structure


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




<a href="https://msdn.microsoft.com/7251c600-90a2-4903-b26a-643b4d10b0ce">IWMAddressAccess Interface</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn927277">Structures</a>
 

 

