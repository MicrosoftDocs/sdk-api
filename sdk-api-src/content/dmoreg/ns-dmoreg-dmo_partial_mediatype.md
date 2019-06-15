---
UID: NS:dmoreg._DMO_PARTIAL_MEDIATYPE
title: DMO_PARTIAL_MEDIATYPE (dmoreg.h)
author: windows-sdk-content
description: The DMO_PARTIAL_MEDIATYPE structure partially describes a media type used by a Microsoft DirectX Media Object (DMO). The DMO registration functions use this structure to specify supported media types.
old-location: dshow\dmo_partial_mediatype.htm
tech.root: DirectShow
ms.assetid: 53bf4c34-d180-4edd-b59a-55d7d90708b5
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PDMO_PARTIAL_MEDIATYPE, DMO_PARTIAL_MEDIATYPE, DMO_PARTIAL_MEDIATYPE structure [DirectShow], DMO_PARTIAL_MEDIATYPEStructure, PDMO_PARTIAL_MEDIATYPE, PDMO_PARTIAL_MEDIATYPE structure pointer [DirectShow], dmoreg/DMO_PARTIAL_MEDIATYPE, dmoreg/PDMO_PARTIAL_MEDIATYPE, dshow.dmo_partial_mediatype"
ms.topic: struct
f1_keywords: ["dmoreg/DMO_PARTIAL_MEDIATYPE"]
req.header: dmoreg.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Dmoreg.h
api_name:
 - DMO_PARTIAL_MEDIATYPE
product: Windows
targetos: Windows
req.typenames: DMO_PARTIAL_MEDIATYPE, *PDMO_PARTIAL_MEDIATYPE
req.redist: 
ms.custom: 19H1
---

# DMO_PARTIAL_MEDIATYPE structure


## -description



The <code>DMO_PARTIAL_MEDIATYPE</code> structure partially describes a media type used by a Microsoft DirectX Media Object (DMO). The DMO registration functions use this structure to specify supported media types.




## -struct-fields




### -field type

Major type GUID. Use GUID_NULL to match any major type.


### -field subtype

Subtype GUID. Use GUID_NULL to match any subtype.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/dmo-structures">DMO Structures</a>
 

 

