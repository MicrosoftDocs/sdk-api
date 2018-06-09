---
UID: NS:mpeg2bits.MPEG_HEADER_BITS
title: MPEG_HEADER_BITS
author: windows-sdk-content
description: The MPEG_HEADER_BITS structure contains the first 16 bits that follow the table_id in a generic MPEG-2 section header.
old-location: mstv\mpeg_header_bits.htm
old-project: mstv
ms.assetid: e25d36af-ee72-4986-8d96-2bce8b19ac80
ms.author: windowssdkdev
ms.date: 06/06/2018
ms.keywords: "*PMPEG_HEADER_BITS, MPEG_HEADER_BITS, MPEG_HEADER_BITS structure [Microsoft TV Technologies], MPEG_HEADER_BITSStructure, PMPEG_HEADER_BITS, PMPEG_HEADER_BITS structure pointer [Microsoft TV Technologies], mpeg2bits/MPEG_HEADER_BITS, mpeg2bits/PMPEG_HEADER_BITS, mstv.mpeg_header_bits"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: mpeg2bits.h
req.include-header: Mpeg2Structs.h
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
tech.root: 
req.typenames: MPEG_HEADER_BITS, *PMPEG_HEADER_BITS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mpeg2Bits.h
api_name:
 - MPEG_HEADER_BITS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# MPEG_HEADER_BITS structure


## -description



The <b>MPEG_HEADER_BITS</b> structure contains the first 16 bits that follow the table_id in a generic MPEG-2 section header.




## -struct-fields




### -field SectionLength


            The length of the section, in bytes.
          


### -field Reserved


            Two reserved bits.
          


### -field PrivateIndicator


            The private_indicator bit.
          


### -field SectionSyntaxIndicator


            The section_syntax_indicator bit.
          


## -see-also




<a href="https://msdn.microsoft.com/5ae43ac6-519d-486b-aaa5-c766f3194ef2">BDA Structures</a>



<a href="https://msdn.microsoft.com/6ee07b84-ae97-413f-a3b4-0078ad740194">SECTION Structure</a>
 

 

