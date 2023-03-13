---
UID: NE:msinkaut.InkPersistenceFormat
title: InkPersistenceFormat (msinkaut.h)
description: Specifies how ink is persisted.
helpviewer_keywords: ["IPF_Base64Gif","IPF_Base64InkSerializedFormat","IPF_Gif","IPF_InkSerializedFormat","InkPersistenceFormat","InkPersistenceFormat enumeration [Tablet PC]","ecbf48ce-0394-4da1-9f5c-d2626545982c","msinkaut/IPF_Base64Gif","msinkaut/IPF_Base64InkSerializedFormat","msinkaut/IPF_Gif","msinkaut/IPF_InkSerializedFormat","msinkaut/InkPersistenceFormat","tablet.inkpersistenceformat"]
old-location: tablet\inkpersistenceformat.htm
tech.root: tablet
ms.assetid: ecbf48ce-0394-4da1-9f5c-d2626545982c
ms.date: 12/05/2018
ms.keywords: IPF_Base64Gif, IPF_Base64InkSerializedFormat, IPF_Gif, IPF_InkSerializedFormat, InkPersistenceFormat, InkPersistenceFormat enumeration [Tablet PC], ecbf48ce-0394-4da1-9f5c-d2626545982c, msinkaut/IPF_Base64Gif, msinkaut/IPF_Base64InkSerializedFormat, msinkaut/IPF_Gif, msinkaut/IPF_InkSerializedFormat, msinkaut/InkPersistenceFormat, tablet.inkpersistenceformat
req.header: msinkaut.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP Tablet PC Edition [desktop apps only]
req.target-min-winversvr: None supported
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
targetos: Windows
req.typenames: InkPersistenceFormat
req.redist: 
ms.custom: 19H1
f1_keywords:
 - InkPersistenceFormat
 - msinkaut/InkPersistenceFormat
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - msinkaut.h
api_name:
 - InkPersistenceFormat
---

# InkPersistenceFormat enumeration


## -description

Specifies how ink is persisted.

## -enum-fields

### -field IPF_InkSerializedFormat:0

Ink is persisted using ink serialized format (ISF).

This is the most compact persistent representation of ink. It can be embedded within a binary document format or placed directly on the Clipboard.

### -field IPF_Base64InkSerializedFormat:1

Ink is persisted by encoding the ISF as a base64 stream.

This format is provided so that ink can be encoded directly in an Extensible Markup Language (XML) or HTML file.

### -field IPF_GIF:2

Ink is persisted by using a Graphics Interchange Format (GIF) file that contains ISF as metadata that is embedded within the file.

This allows ink to be viewed in applications that are not ink-enabled and maintain its full ink fidelity when it returns to an ink-enabled application. This format is ideal when transporting ink content within an HTML file and making it usable by ink-enabled and ink-unaware applications.

### -field IPF_Base64GIF:3

Ink is persisted by using a base64 encoded fortified.

This GIF format is provided when ink is to be encoded directly in an XML or HTML file with later conversion into an image. A possible use of this would be in an XML format that is generated to contain all ink information and used as a way to generate HTML through Extensible Stylesheet Language Transformations (XSLT).


## -see-also

<a href="/windows/desktop/tablet/inkdisp-class">InkDisp Class</a>



<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-save">Save Method [InkDisp Class]</a>
