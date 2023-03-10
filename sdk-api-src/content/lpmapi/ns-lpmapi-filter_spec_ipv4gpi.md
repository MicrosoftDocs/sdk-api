---
UID: NS:lpmapi.Filter_Spec_IPv4GPI
title: Filter_Spec_IPv4GPI (lpmapi.h)
description: The Filter_Spec_IPv4GPI structure contains generalized port ID information about an IPv4 FILTERSPEC.
helpviewer_keywords: ["Filter_Spec_IPv4GPI","Filter_Spec_IPv4GPI structure [QOS]","lpmapi/Filter_Spec_IPv4GPI","qos.filter_spec_ipv4gpi"]
old-location: qos\filter_spec_ipv4gpi.htm
tech.root: QOS
ms.assetid: c1546673-d1b5-4a7f-82d0-a8cc1c7c8752
ms.date: 12/05/2018
ms.keywords: Filter_Spec_IPv4GPI, Filter_Spec_IPv4GPI structure [QOS], lpmapi/Filter_Spec_IPv4GPI, qos.filter_spec_ipv4gpi
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
req.typenames: Filter_Spec_IPv4GPI
req.redist: 
ms.custom: 19H1
f1_keywords:
 - Filter_Spec_IPv4GPI
 - lpmapi/Filter_Spec_IPv4GPI
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Lpmapi.h
api_name:
 - Filter_Spec_IPv4GPI
---

# Filter_Spec_IPv4GPI structure


## -description

The 
<b>Filter_Spec_IPv4GPI</b> structure contains generalized port ID information about an IPv4 FILTERSPEC.

## -struct-fields

### -field filt_ipaddr

IP address of the source address, in the form of an <a href="/windows/desktop/api/winsock2/ns-winsock2-in_addr">in_addr</a> structure.

### -field filt_gpi

Generalized Port Identifier.

## -see-also

<a href="/windows/desktop/api/winsock2/ns-winsock2-in_addr">in_addr</a>

