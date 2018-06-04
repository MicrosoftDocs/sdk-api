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
 

 

