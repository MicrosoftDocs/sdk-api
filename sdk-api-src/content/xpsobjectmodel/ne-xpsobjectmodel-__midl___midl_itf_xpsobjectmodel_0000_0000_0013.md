---
UID: NE:xpsobjectmodel.__MIDL___MIDL_itf_xpsobjectmodel_0000_0000_0013
title: "__MIDL___MIDL_itf_xpsobjectmodel_0000_0000_0013"
author: windows-sdk-content
description: Describes the option for embedding a font.
old-location: xps\xps_font_embedding.htm
old-project: printdocs
ms.assetid: 9701b1c2-a909-410e-b05b-76bbd5bc8b44
ms.author: windowssdkdev
ms.date: 06/05/2018
ms.keywords: XPS_FONT_EMBEDDING, XPS_FONT_EMBEDDING enumeration [XPS Documents and Packaging], XPS_FONT_EMBEDDING_NORMAL, XPS_FONT_EMBEDDING_OBFUSCATED, XPS_FONT_EMBEDDING_RESTRICTED, XPS_FONT_EMBEDDING_RESTRICTED_UNOBFUSCATED, __MIDL___MIDL_itf_xpsobjectmodel_0000_0000_0013, xps.xps_font_embedding, xpsobjectmodel/XPS_FONT_EMBEDDING, xpsobjectmodel/XPS_FONT_EMBEDDING_NORMAL, xpsobjectmodel/XPS_FONT_EMBEDDING_OBFUSCATED, xpsobjectmodel/XPS_FONT_EMBEDDING_RESTRICTED, xpsobjectmodel/XPS_FONT_EMBEDDING_RESTRICTED_UNOBFUSCATED
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
req.typenames: XPS_FONT_EMBEDDING
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - xpsobjectmodel.h
api_name:
 - XPS_FONT_EMBEDDING
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# __MIDL___MIDL_itf_xpsobjectmodel_0000_0000_0013 enumeration


## -description


Describes the option for embedding a font.


## -enum-fields




### -field XPS_FONT_EMBEDDING_NORMAL

The embedded font is neither obfuscated nor restricted.


### -field XPS_FONT_EMBEDDING_OBFUSCATED

The embedded font is obfuscated but not restricted.


### -field XPS_FONT_EMBEDDING_RESTRICTED

The embedded font is obfuscated and restricted.


### -field XPS_FONT_EMBEDDING_RESTRICTED_UNOBFUSCATED

The font is restricted but not obfuscated.

This value cannot be set by an application. It is set when the document being deserialized contains a restricted font that is not obfuscated. Restricted fonts should be obfuscated, so this value usually indicates an error in the application that created the XPS document being deserialized.


## -see-also




<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>
 

 

