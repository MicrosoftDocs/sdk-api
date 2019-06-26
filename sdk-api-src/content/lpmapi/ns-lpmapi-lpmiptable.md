---
UID: NS:lpmapi.lpmiptable
title: LPMIPTABLE (lpmapi.h)
author: windows-sdk-content
description: The LPMIPTABLE structure contains IP information, including the SNMP index, IP address, and subnet mask for each interface. The LPMIPTABLE structure is supplied as an argument for the Lpm_IpAddressTable function.
old-location: qos\lpmiptable.htm
tech.root: QOS
ms.assetid: cbd67aa2-8b87-4e24-8a8e-a6c60cebf31f
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: LPMIPTABLE, LPMIPTABLE structure [QOS], _gqos_lpmiptable, lpmapi/LPMIPTABLE, qos.lpmiptable
ms.topic: struct
f1_keywords: 
 - "lpmapi/LPMIPTABLE"
req.header: lpmapi.h
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Lpmapi.h
api_name:
 - LPMIPTABLE
product: Windows
targetos: Windows
req.typenames: LPMIPTABLE
req.redist: 
ms.custom: 19H1
---

# LPMIPTABLE structure


## -description


The 
<b>LPMIPTABLE</b> structure contains IP information, including the SNMP index, IP address, and subnet mask for each interface. The 
<b>LPMIPTABLE</b> structure is supplied as an argument for the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/lpmapi/nf-lpmapi-lpm_ipaddresstable">Lpm_IpAddressTable</a> function.


## -struct-fields




### -field ulIfIndex

 


### -field MediaType

Media type of the interface.


### -field IfIpAddr

IP address for the interface.


### -field IfNetMask

IP subnet mask for the interface.


#### - UlIfIndex

SNMP index for the interface.


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/lpmapi/nf-lpmapi-lpm_ipaddresstable">Lpm_IpAddressTable</a>
 

 

