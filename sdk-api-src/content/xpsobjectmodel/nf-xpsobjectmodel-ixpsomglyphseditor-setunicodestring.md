---
UID: NF:xpsobjectmodel.IXpsOMGlyphsEditor.SetUnicodeString
title: IXpsOMGlyphsEditor::SetUnicodeString (xpsobjectmodel.h)
description: Sets the text in unescaped UTF-16 scalar values.
helpviewer_keywords: ["IXpsOMGlyphsEditor interface [XPS Documents and Packaging]","SetUnicodeString method","IXpsOMGlyphsEditor.SetUnicodeString","IXpsOMGlyphsEditor::SetUnicodeString","SetUnicodeString","SetUnicodeString method [XPS Documents and Packaging]","SetUnicodeString method [XPS Documents and Packaging]","IXpsOMGlyphsEditor interface","xps.ixpsomglyphseditor_setunicodestring","xpsobjectmodel/IXpsOMGlyphsEditor::SetUnicodeString"]
old-location: xps\ixpsomglyphseditor_setunicodestring.htm
tech.root: xps
ms.assetid: 68d5ab7d-63e4-403d-a689-6fc0a10e007c
ms.date: 12/05/2018
ms.keywords: IXpsOMGlyphsEditor interface [XPS Documents and Packaging],SetUnicodeString method, IXpsOMGlyphsEditor.SetUnicodeString, IXpsOMGlyphsEditor::SetUnicodeString, SetUnicodeString, SetUnicodeString method [XPS Documents and Packaging], SetUnicodeString method [XPS Documents and Packaging],IXpsOMGlyphsEditor interface, xps.ixpsomglyphseditor_setunicodestring, xpsobjectmodel/IXpsOMGlyphsEditor::SetUnicodeString
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IXpsOMGlyphsEditor::SetUnicodeString
 - xpsobjectmodel/IXpsOMGlyphsEditor::SetUnicodeString
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - xpsobjectmodel.h
api_name:
 - IXpsOMGlyphsEditor.SetUnicodeString
---

# IXpsOMGlyphsEditor::SetUnicodeString


## -description

Sets the text in unescaped UTF-16 scalar values.

## -parameters

### -param unicodeString [in]

The address of a UTF-16 Unicode string. A <b>NULL</b> pointer clears the property.

## -returns

If the method succeeds, it returns S_OK; otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphseditor">IXpsOMGlyphsEditor</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>