---
UID: NS:xpsobjectmodel.__MIDL___MIDL_itf_xpsobjectmodel_0000_0000_0022
title: "__MIDL___MIDL_itf_xpsobjectmodel_0000_0000_0022"
author: windows-sdk-content
description: Describes a glyph-to-index mapping.
old-location: xps\xps_glyph_mapping.htm
old-project: printdocs
ms.assetid: 5cc76cba-66e4-4853-969b-a99ec7bb22f3
ms.author: windowssdkdev
ms.date: 05/23/2018
ms.keywords: XPS_GLYPH_MAPPING, XPS_GLYPH_MAPPING structure [XPS Documents and Packaging], __MIDL___MIDL_itf_xpsobjectmodel_0000_0000_0022, xps.xps_glyph_mapping, xpsobjectmodel/XPS_GLYPH_MAPPING
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: xpsobjectmodel.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: XpsObjectModel.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: XPS_GLYPH_MAPPING
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	xpsobjectmodel.h
api_name:
-	XPS_GLYPH_MAPPING
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# __MIDL___MIDL_itf_xpsobjectmodel_0000_0000_0022 structure


## -description


Describes a glyph-to-index mapping.


## -struct-fields




### -field unicodeStringStart

Index of the first Unicode character in the mapping string.


### -field unicodeStringLength

Number of characters in the mapping string.


### -field glyphIndicesStart

The glyph array's first  index that corresponds to <b>unicodeStringStart</b>.


### -field glyphIndicesLength

Length of index mapping.


## -see-also




<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>
 

 

