---
UID: NS:dmoreg._DMO_PARTIAL_MEDIATYPE
title: "_DMO_PARTIAL_MEDIATYPE"
author: windows-sdk-content
description: The DMO_PARTIAL_MEDIATYPE structure partially describes a media type used by a Microsoft DirectX Media Object (DMO). The DMO registration functions use this structure to specify supported media types.
old-location: dshow\dmo_partial_mediatype.htm
old-project: DirectShow
ms.assetid: 53bf4c34-d180-4edd-b59a-55d7d90708b5
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: "*PDMO_PARTIAL_MEDIATYPE, DMO_PARTIAL_MEDIATYPE, DMO_PARTIAL_MEDIATYPE structure [DirectShow], DMO_PARTIAL_MEDIATYPEStructure, PDMO_PARTIAL_MEDIATYPE, PDMO_PARTIAL_MEDIATYPE structure pointer [DirectShow], _DMO_PARTIAL_MEDIATYPE, dmoreg/DMO_PARTIAL_MEDIATYPE, dmoreg/PDMO_PARTIAL_MEDIATYPE, dshow.dmo_partial_mediatype"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
tech.root: 
req.typenames: DMO_PARTIAL_MEDIATYPE, *PDMO_PARTIAL_MEDIATYPE
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
req.lib: 
req.dll: 
req.irql: 
---

# _DMO_PARTIAL_MEDIATYPE structure


## -description



The <code>DMO_PARTIAL_MEDIATYPE</code> structure partially describes a media type used by a Microsoft DirectX Media Object (DMO). The DMO registration functions use this structure to specify supported media types.




## -struct-fields




### -field type

Major type GUID. Use GUID_NULL to match any major type.


### -field subtype

Subtype GUID. Use GUID_NULL to match any subtype.


## -see-also




<a href="https://msdn.microsoft.com/82c8ea74-1c5e-4370-9075-6db2ed6b2c91">DMO Structures</a>
 

 

