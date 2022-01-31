---
UID: NE:xpsobjectmodel.__MIDL___MIDL_itf_xpsobjectmodel_0000_0000_0013
title: XPS_FONT_EMBEDDING (xpsobjectmodel.h)
description: Describes the option for embedding a font.
helpviewer_keywords: ["XPS_FONT_EMBEDDING","XPS_FONT_EMBEDDING enumeration [XPS Documents and Packaging]","XPS_FONT_EMBEDDING_NORMAL","XPS_FONT_EMBEDDING_OBFUSCATED","XPS_FONT_EMBEDDING_RESTRICTED","XPS_FONT_EMBEDDING_RESTRICTED_UNOBFUSCATED","xps.xps_font_embedding","xpsobjectmodel/XPS_FONT_EMBEDDING","xpsobjectmodel/XPS_FONT_EMBEDDING_NORMAL","xpsobjectmodel/XPS_FONT_EMBEDDING_OBFUSCATED","xpsobjectmodel/XPS_FONT_EMBEDDING_RESTRICTED","xpsobjectmodel/XPS_FONT_EMBEDDING_RESTRICTED_UNOBFUSCATED"]
old-location: xps\xps_font_embedding.htm
tech.root: xps
ms.assetid: 9701b1c2-a909-410e-b05b-76bbd5bc8b44
ms.date: 12/05/2018
ms.keywords: XPS_FONT_EMBEDDING, XPS_FONT_EMBEDDING enumeration [XPS Documents and Packaging], XPS_FONT_EMBEDDING_NORMAL, XPS_FONT_EMBEDDING_OBFUSCATED, XPS_FONT_EMBEDDING_RESTRICTED, XPS_FONT_EMBEDDING_RESTRICTED_UNOBFUSCATED, xps.xps_font_embedding, xpsobjectmodel/XPS_FONT_EMBEDDING, xpsobjectmodel/XPS_FONT_EMBEDDING_NORMAL, xpsobjectmodel/XPS_FONT_EMBEDDING_OBFUSCATED, xpsobjectmodel/XPS_FONT_EMBEDDING_RESTRICTED, xpsobjectmodel/XPS_FONT_EMBEDDING_RESTRICTED_UNOBFUSCATED
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
req.typenames: XPS_FONT_EMBEDDING
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL___MIDL_itf_xpsobjectmodel_0000_0000_0013
 - xpsobjectmodel/__MIDL___MIDL_itf_xpsobjectmodel_0000_0000_0013
 - XPS_FONT_EMBEDDING
 - xpsobjectmodel/XPS_FONT_EMBEDDING
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
 - XPS_FONT_EMBEDDING
---

# XPS_FONT_EMBEDDING enumeration


## -description

Describes the option for embedding a font.

## -enum-fields

### -field XPS_FONT_EMBEDDING_NORMAL:1

The embedded font is neither obfuscated nor restricted.

### -field XPS_FONT_EMBEDDING_OBFUSCATED

The embedded font is obfuscated but not restricted.

### -field XPS_FONT_EMBEDDING_RESTRICTED

The embedded font is obfuscated and restricted.

### -field XPS_FONT_EMBEDDING_RESTRICTED_UNOBFUSCATED

The font is restricted but not obfuscated.

This value cannot be set by an application. It is set when the document being deserialized contains a restricted font that is not obfuscated. Restricted fonts should be obfuscated, so this value usually indicates an error in the application that created the XPS document being deserialized.

## -see-also

<a href="https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf">XML Paper Specification</a>

