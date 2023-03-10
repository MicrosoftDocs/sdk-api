---
UID: NE:xpsobjectmodel.__MIDL___MIDL_itf_xpsobjectmodel_0000_0000_0016
title: XPS_INTERLEAVING (xpsobjectmodel.h)
description: Specifies whether the content of the XPS OM will be interleaved when it is written to a file or a stream.
helpviewer_keywords: ["XPS_INTERLEAVING","XPS_INTERLEAVING enumeration [XPS Documents and Packaging]","XPS_INTERLEAVING_OFF","XPS_INTERLEAVING_ON","xps.xps_interleaving","xpsobjectmodel/XPS_INTERLEAVING","xpsobjectmodel/XPS_INTERLEAVING_OFF","xpsobjectmodel/XPS_INTERLEAVING_ON"]
old-location: xps\xps_interleaving.htm
tech.root: xps
ms.assetid: cfb2d1f3-2edb-4342-9fcc-c058afa3ef83
ms.date: 12/05/2018
ms.keywords: XPS_INTERLEAVING, XPS_INTERLEAVING enumeration [XPS Documents and Packaging], XPS_INTERLEAVING_OFF, XPS_INTERLEAVING_ON, xps.xps_interleaving, xpsobjectmodel/XPS_INTERLEAVING, xpsobjectmodel/XPS_INTERLEAVING_OFF, xpsobjectmodel/XPS_INTERLEAVING_ON
req.header: xpsobjectmodel.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: XpsObjectModel.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: XPS_INTERLEAVING
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL___MIDL_itf_xpsobjectmodel_0000_0000_0016
 - xpsobjectmodel/__MIDL___MIDL_itf_xpsobjectmodel_0000_0000_0016
 - XPS_INTERLEAVING
 - xpsobjectmodel/XPS_INTERLEAVING
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - xpsobjectmodel.h
api_name:
 - XPS_INTERLEAVING
---

# XPS_INTERLEAVING enumeration


## -description

Specifies whether the content of the XPS OM will be interleaved when it is written to a file or a stream.

## -enum-fields

### -field XPS_INTERLEAVING_OFF:1

The content of the XPS OM is not interleaved. The document parts are written as complete parts.

### -field XPS_INTERLEAVING_ON

The content of the XPS OM is interleaved. The document parts are divided into smaller pieces before they are written.

## -see-also

<a href="https://www.ecma-international.org/publications/standards/Ecma-376.htm">Standard ECMA-376, Office Open XML File Formats</a>



<a href="https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf">XML Paper Specification</a>

