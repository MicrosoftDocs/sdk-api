---
UID: NS:qossp._RSVP_FILTERSPEC_V6
title: "_RSVP_FILTERSPEC_V6"
author: windows-sdk-content
description: The RSVP_FILTERSPEC_V6 structure stores information for a FILTERSPEC on an IPv6 address.
old-location: qos\rsvp_filterspec_v6.htm
tech.root: QOS
ms.assetid: 7e567714-1d91-4dd4-a560-2b57876c837c
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: "*LPRSVP_FILTERSPEC_V6, RSVP_FILTERSPEC_V6, RSVP_FILTERSPEC_V6 structure [QOS], _RSVP_FILTERSPEC_V6, qos.rsvp_filterspec_v6, qossp/RSVP_FILTERSPEC_V6"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: qossp.h
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
 - Qossp.h
api_name:
 - RSVP_FILTERSPEC_V6
product: Windows
targetos: Windows
req.typenames: RSVP_FILTERSPEC_V6, *LPRSVP_FILTERSPEC_V6
req.redist: 
---

# _RSVP_FILTERSPEC_V6 structure


## -description


The <b>RSVP_FILTERSPEC_V6</b> structure  stores information for a FILTERSPEC on an IPv6 address.


## -struct-fields




### -field Address

IPv4 address for which the FILTERSPEC applies, expressed as an <a href="https://msdn.microsoft.com/e21edb47-c704-415f-901b-7612e5157ab0">IN_ADDR_IPV6</a> structure.


### -field UnUsed

 


### -field Port

TCP port of the socket on which the FILTERSPEC applies.


#### - Unused

Reserved. Set to zero.


## -remarks



When working with IPv4 addresses, use <a href="https://msdn.microsoft.com/038edc41-7324-4c5a-8172-c958cee05d5e">RSVP_FILTERSPEC_V4</a>.




## -see-also




<a href="https://msdn.microsoft.com/e21edb47-c704-415f-901b-7612e5157ab0">IN_ADDR_IPV6</a>



<a href="https://msdn.microsoft.com/038edc41-7324-4c5a-8172-c958cee05d5e">RSVP_FILTERSPEC_V4</a>
 

 

