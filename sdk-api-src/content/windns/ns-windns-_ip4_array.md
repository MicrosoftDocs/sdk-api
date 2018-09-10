---
UID: NS:windns._IP4_ARRAY
title: "_IP4_ARRAY"
author: windows-sdk-content
description: The IP4_ARRAY structure stores an array of IPv4 addresses.
old-location: dns\ip4_array.htm
tech.root: dns
ms.assetid: 4273a739-129c-4951-b6df-aef4332ce0cb
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: "*PIP4_ARRAY, *PIP4_ARRAY structure [DNS], IP4_ARRAY, IP4_ARRAY structure [DNS], _IP4_ARRAY, dns.ip4_array, windns/*PIP4_ARRAY, windns/IP4_ARRAY"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: windns.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - Windns.h
api_name:
 - IP4_ARRAY
product: Windows
targetos: Windows
req.typenames: IP4_ARRAY, *PIP4_ARRAY
req.redist: 
---

# _IP4_ARRAY structure


## -description


The <b>IP4_ARRAY</b> structure stores an array of IPv4 addresses.


## -struct-fields




### -field AddrCount

The number of IPv4 addresses in <b>AddrArray</b>.


### -field AddrArray.size_is

 


### -field AddrArray.size_is.AddrCount

 


### -field AddrArray

An array of <a href="https://msdn.microsoft.com/652012a5-e45d-4ea6-896a-17e8b1ed4a05">IP4_ADDRESS</a> data types that contains a list of IPv4 address.

