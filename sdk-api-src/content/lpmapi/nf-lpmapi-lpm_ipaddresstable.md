---
UID: NF:lpmapi.LPM_IpAddressTable
title: LPM_IpAddressTable function (lpmapi.h)
description: The LPM_IpAddressTable function is used by the PCM to pass a list of IP addresses assigned to the Windows 2000 Server upon which the LPM is initialized.
helpviewer_keywords: ["LPM_IpAddressTable","LPM_IpAddressTable callback","LPM_IpAddressTable callback function [QOS]","_gqos_lpm_ipaddresstable","lpmapi/LPM_IpAddressTable","qos.lpm_ipaddresstable"]
old-location: qos\lpm_ipaddresstable.htm
tech.root: QOS
ms.assetid: f02ecb97-3797-49a0-8bff-fcb16096cb25
ms.date: 12/05/2018
ms.keywords: LPM_IpAddressTable, LPM_IpAddressTable callback, LPM_IpAddressTable callback function [QOS], _gqos_lpm_ipaddresstable, lpmapi/LPM_IpAddressTable, qos.lpm_ipaddresstable
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - LPM_IpAddressTable
 - lpmapi/LPM_IpAddressTable
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Lpmapi.h
api_name:
 - LPM_IpAddressTable
---

# LPM_IpAddressTable function


## -description

The 
<i>LPM_IpAddressTable</i> function is used by the PCM to pass a list of IP addresses assigned to the Windows 2000 Server upon which the LPM is initialized. The PCM calls this routine after the LPM has successfully initialized, but before making any requests. The PCM also uses the 
<i>LPM_IpAddressTable</i> function to update LPMs regarding IP address changes. LPMs are expected to detect IP address changes and update their states appropriately.

## -parameters

### -param cIpAddrTable [in]

Number of addresses in the IP table.

### -param pIpAddrTable [in]

Pointer to an 
<a href="/previous-versions/windows/desktop/api/lpmapi/ns-lpmapi-lpmiptable">LPMIPTABLE</a> structure that contains the IP addresses assigned to the Windows 2000 Server on which the LPM resides.

## -returns

Returns <b>TRUE</b> if successful, or <b>FALSE</b> otherwise.

## -see-also

<a href="/previous-versions/windows/desktop/api/lpmapi/ns-lpmapi-lpmiptable">LPMIPTABLE</a>