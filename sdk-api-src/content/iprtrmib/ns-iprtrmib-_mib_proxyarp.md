---
UID: NS:iprtrmib._MIB_PROXYARP
title: "_MIB_PROXYARP"
author: windows-sdk-content
description: Stores information for a Proxy Address Resolution Protocol (PARP) entry.
old-location: mib\mib_proxyarp.htm
old-project: MIB
ms.assetid: 4f919bfb-733b-4b49-8550-505626779eac
ms.author: windowssdkdev
ms.date: 05/14/2018
ms.keywords: "*PMIB_PROXYARP, MIB_PROXYARP, MIB_PROXYARP structure [MIB], PMIB_PROXYARP, PMIB_PROXYARP structure pointer [MIB], _MIB_PROXYARP, _mpr_mib_proxyarp, iprtrmib/MIB_PROXYARP, iprtrmib/PMIB_PROXYARP, mib.mib_proxyarp, rras.mib_proxyarp"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
tech.root: 
req.typenames: MIB_PROXYARP, *PMIB_PROXYARP
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Iprtrmib.h
api_name:
 - MIB_PROXYARP
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# _MIB_PROXYARP structure


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




<a href="https://docs.microsoft.com/windows/desktop/api/iphlpapi/nf-iphlpapi-createproxyarpentry">CreateProxyArpEntry</a>



<a href="https://docs.microsoft.com/windows/desktop/api/iphlpapi/nf-iphlpapi-deleteproxyarpentry">DeleteProxyArpEntry</a>
 

 

