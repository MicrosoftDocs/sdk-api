---
UID: NE:vdshwprv.VDS_IPADDRESS_TYPE
title: VDS_IPADDRESS_TYPE
author: windows-sdk-content
description: Defines the set of valid types for an IP address.
old-location: base\vds_ipaddress_type.htm
tech.root: VDS
ms.assetid: 9121957f-1626-4d52-9749-0a769fece5fa
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: VDS_IPADDRESS_TYPE, VDS_IPADDRESS_TYPE enumeration [VDS], VDS_IPT_EMPTY, VDS_IPT_IPV4, VDS_IPT_IPV6, VDS_IPT_TEXT, base.vds_ipaddress_type, vds/VDS_IPADDRESS_TYPE, vds/VDS_IPT_EMPTY, vds/VDS_IPT_IPV4, vds/VDS_IPT_IPV6, vds/VDS_IPT_TEXT, vdshwprv/VDS_IPADDRESS_TYPE, vdshwprv/VDS_IPT_EMPTY, vdshwprv/VDS_IPT_IPV4, vdshwprv/VDS_IPT_IPV6, vdshwprv/VDS_IPT_TEXT
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: vdshwprv.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 R2 [desktop apps only]
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
 - Vds.h
 - VdsHwPrv.h
api_name:
 - VDS_IPADDRESS_TYPE
product: Windows
targetos: Windows
req.typenames: VDS_IPADDRESS_TYPE
req.redist: VDS 1.1
---

# VDS_IPADDRESS_TYPE enumeration


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Defines the set of valid types for an IP address. These values are used in the 
   <b>type</b> member of the 
   <a href="https://msdn.microsoft.com/42e8b161-5e47-4aae-aa23-94b5cacb5698">VDS_IPADDRESS</a> structure.


## -enum-fields




### -field VDS_IPT_TEXT

The address is a text address that is either a DNS address, an IPv4 dotted address, or an IPv6 hex 
      address.


### -field VDS_IPT_IPV4

The address is an IPv4 address in binary format.


### -field VDS_IPT_IPV6

The address is an IPv6 address in binary format.


### -field VDS_IPT_EMPTY

The address is empty.


## -remarks



<div class="alert"><b>Note</b>  Additional constants might be added to the <b>VDS_IPADDRESS_TYPE</b> enumeration in future Windows versions. For this reason, your application must be designed to gracefully handle an unrecognized <b>VDS_IPADDRESS_TYPE</b> enumeration constant.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/30ee6e39-c1e5-4173-a3dd-5644632140d1">VDS Enumerations</a>



<a href="https://msdn.microsoft.com/42e8b161-5e47-4aae-aa23-94b5cacb5698">VDS_IPADDRESS</a>
 

 

