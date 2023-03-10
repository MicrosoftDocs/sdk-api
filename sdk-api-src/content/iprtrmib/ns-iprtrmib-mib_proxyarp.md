---
UID: NS:iprtrmib._MIB_PROXYARP
title: MIB_PROXYARP (iprtrmib.h)
description: Stores information for a Proxy Address Resolution Protocol (PARP) entry.
helpviewer_keywords: ["*PMIB_PROXYARP","MIB_PROXYARP","MIB_PROXYARP structure [MIB]","PMIB_PROXYARP","PMIB_PROXYARP structure pointer [MIB]","_mpr_mib_proxyarp","iprtrmib/MIB_PROXYARP","iprtrmib/PMIB_PROXYARP","mib.mib_proxyarp","rras.mib_proxyarp"]
old-location: mib\mib_proxyarp.htm
tech.root: MIB
ms.assetid: 4f919bfb-733b-4b49-8550-505626779eac
ms.date: 12/05/2018
ms.keywords: '*PMIB_PROXYARP, MIB_PROXYARP, MIB_PROXYARP structure [MIB], PMIB_PROXYARP, PMIB_PROXYARP structure pointer [MIB], _mpr_mib_proxyarp, iprtrmib/MIB_PROXYARP, iprtrmib/PMIB_PROXYARP, mib.mib_proxyarp, rras.mib_proxyarp'
req.header: iprtrmib.h
req.include-header: Iphlpapi.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: MIB_PROXYARP, *PMIB_PROXYARP
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MIB_PROXYARP
 - iprtrmib/_MIB_PROXYARP
 - PMIB_PROXYARP
 - iprtrmib/PMIB_PROXYARP
 - MIB_PROXYARP
 - iprtrmib/MIB_PROXYARP
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Iprtrmib.h
api_name:
 - MIB_PROXYARP
---

# MIB_PROXYARP structure


## -description

The 
<b>MIB_PROXYARP</b> structure stores information for a Proxy Address Resolution Protocol (PARP) entry.

## -struct-fields

### -field dwAddress

The IPv4 address for which to act as a proxy.

### -field dwMask

The subnet mask for the IPv4 address specified by the <b>dwAddress</b> member.

### -field dwIfIndex

The index of the interface on which to act as a proxy for the address specified by the <b>dwAddress</b> member.

## -see-also

<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-createproxyarpentry">CreateProxyArpEntry</a>



<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-deleteproxyarpentry">DeleteProxyArpEntry</a>