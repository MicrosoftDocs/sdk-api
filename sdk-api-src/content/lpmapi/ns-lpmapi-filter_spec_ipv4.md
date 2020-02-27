---
UID: NS:lpmapi.__unnamed_struct_6
title: Filter_Spec_IPv4 (lpmapi.h)
description: The Filter_Spec_IPv4 structure contains information about an IPv4 FILTERSPEC.
old-location: qos\filter_spec_ipv4.htm
tech.root: QOS
ms.assetid: b17a45b2-e50b-4ec2-9f1c-e1ab80ce572e
ms.date: 12/05/2018
ms.keywords: Filter_Spec_IPv4, Filter_Spec_IPv4 structure [QOS], lpmapi/Filter_Spec_IPv4, qos.filter_spec_ipv4
f1_keywords:
- lpmapi/Filter_Spec_IPv4
dev_langs:
- c++
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
- Filter_Spec_IPv4
targetos: Windows
req.typenames: Filter_Spec_IPv4
req.redist: 
ms.custom: 19H1
---

# Filter_Spec_IPv4 structure


## -description


The 
<b>Filter_Spec_IPv4</b> structure contains information about an IPv4 FILTERSPEC.


## -struct-fields




### -field filt_ipaddr

IP address of the source address, in the form of an <a href="https://docs.microsoft.com/windows/desktop/api/winsock2/ns-winsock2-in_addr">in_addr</a> structure.


### -field filt_unused

Reserved. Do not use.


### -field filt_port

TCP port for the source.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/winsock2/ns-winsock2-in_addr">in_addr</a>
 

 

