---
UID: NF:iphlpapi.GetFriendlyIfIndex
title: GetFriendlyIfIndex function (iphlpapi.h)
description: Takes an interface index and returns a backward-compatible interface index, that is, an index that uses only the lower 24 bits.
helpviewer_keywords: ["GetFriendlyIfIndex","GetFriendlyIfIndex function [IP Helper]","_iphlp_getfriendlyifindex","iphlp.getfriendlyifindex","iphlpapi/GetFriendlyIfIndex"]
old-location: iphlp\getfriendlyifindex.htm
tech.root: IpHlp
ms.assetid: 2c5b0b63-cbbb-4e89-be27-8e148a891542
ms.date: 12/05/2018
ms.keywords: GetFriendlyIfIndex, GetFriendlyIfIndex function [IP Helper], _iphlp_getfriendlyifindex, iphlp.getfriendlyifindex, iphlpapi/GetFriendlyIfIndex
req.header: iphlpapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
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
req.lib: Iphlpapi.lib
req.dll: Iphlpapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GetFriendlyIfIndex
 - iphlpapi/GetFriendlyIfIndex
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Iphlpapi.dll
api_name:
 - GetFriendlyIfIndex
---

# GetFriendlyIfIndex function


## -description

The 
<b>GetFriendlyIfIndex</b> function takes an interface index and returns a backward-compatible interface index, that is, an index that uses only the lower 24 bits.

## -parameters

### -param IfIndex [in]

The interface index from which the backward-compatible or "friendly" interface index is derived.

## -returns

A backward-compatible interface index that uses only the lower 24 bits.

## -see-also

<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getifentry">GetIfEntry</a>



<a href="/windows/desktop/IpHlp/ip-helper-function-reference">IP Helper Function Reference</a>



<a href="/windows/desktop/IpHlp/ip-helper-start-page">IP Helper Start Page</a>



<a href="/windows/desktop/api/ifmib/ns-ifmib-mib_ifrow">MIB_IFROW</a>