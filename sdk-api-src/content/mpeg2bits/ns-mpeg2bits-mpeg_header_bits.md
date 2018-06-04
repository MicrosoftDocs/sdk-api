---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
 

 

