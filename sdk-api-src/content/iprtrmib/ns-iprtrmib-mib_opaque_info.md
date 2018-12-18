---
UID: NS:iprtrmib._MIB_OPAQUE_INFO
title: MIB_OPAQUE_INFO
author: windows-sdk-content
description: Contains information returned from a MIB opaque query.
old-location: mib\mib_opaque_info.htm
tech.root: MIB
ms.assetid: d364b08b-80b9-4320-b5bb-e1627d3ce889
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PMIB_OPAQUE_INFO, MIB_OPAQUE_INFO, MIB_OPAQUE_INFO structure [MIB], PMIB_OPAQUE_INFO, PMIB_OPAQUE_INFO structure pointer [MIB], _mpr_mib_opaque_info, iprtrmib/MIB_OPAQUE_INFO, iprtrmib/PMIB_OPAQUE_INFO, mib.mib_opaque_info, rras.mib_opaque_info"
ms.topic: struct
req.header: iprtrmib.h
req.include-header: Iphlpapi.h
req.target-type: Windows
req.target-min-winverclnt: None supported
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
 - Iprtrmib.h
api_name:
 - MIB_OPAQUE_INFO
product: Windows
targetos: Windows
req.typenames: MIB_OPAQUE_INFO, *PMIB_OPAQUE_INFO
req.redist: 
---

# MIB_OPAQUE_INFO structure


## -description


The 
<b>MIB_OPAQUE_INFO</b> structure contains information returned from a MIB opaque query.


## -struct-fields




### -field dwId

The type of information returned.


### -field ullAlign

The number of bytes that align the information returned.


### -field rgbyData

A pointer to the information returned from the opaque query.


## -see-also




<a href="https://msdn.microsoft.com/cd87cbe4-3da4-4205-9a88-becf4f341ab5">MIB_OPAQUE_QUERY</a>
 

 

