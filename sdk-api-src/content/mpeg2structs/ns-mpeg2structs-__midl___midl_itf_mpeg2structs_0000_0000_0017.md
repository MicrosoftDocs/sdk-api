---
UID: NS:mpeg2structs.__MIDL___MIDL_itf_mpeg2structs_0000_0000_0017
title: "__MIDL___MIDL_itf_mpeg2structs_0000_0000_0017"
author: windows-driver-content
description: The ATSC_FILTER_OPTIONS structure specifies additional criteria for matching ATSC section headers.
old-location: mstv\atsc_filter_options.htm
old-project: mstv
ms.assetid: 16e33f92-9e25-4a03-a21f-0ea5a99470ee
ms.author: windowsdriverdev
ms.date: 5/8/2018
ms.keywords: ATSC_FILTER_OPTIONS, ATSC_FILTER_OPTIONS structure [Microsoft TV Technologies], __MIDL___MIDL_itf_mpeg2structs_0000_0000_0017, mpeg2structs/ATSC_FILTER_OPTIONS, mstv.atsc_filter_options
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: mpeg2structs.h
req.include-header: Mpeg2data.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: ATSC_FILTER_OPTIONS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	mpeg2structs.h
api_name:
-	ATSC_FILTER_OPTIONS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# __MIDL___MIDL_itf_mpeg2structs_0000_0000_0017 structure


## -description



The <b>ATSC_FILTER_OPTIONS</b> structure specifies additional criteria for matching ATSC section headers.




## -struct-fields




### -field fSpecifyEtmId

If this flag is <b>TRUE</b>, the ETM_id field in the header must match the value of the <b>EtmId</b> structure member. Otherwise, the ETM_id field is ignored.


### -field EtmId

Specifies a value for the ETM_id field.


## -see-also




<a href="https://msdn.microsoft.com/5ae43ac6-519d-486b-aaa5-c766f3194ef2">BDA Structures</a>



<a href="https://msdn.microsoft.com/a7e66de7-d67b-4814-9849-076c3dd5afb1">MPEG2_FILTER Structure</a>
 

 

