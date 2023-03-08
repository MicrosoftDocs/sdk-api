---
UID: NF:xpsobjectmodel.IXpsOMCoreProperties.SetContentType
title: IXpsOMCoreProperties::SetContentType (xpsobjectmodel.h)
description: Sets the contentType property.
helpviewer_keywords: ["IXpsOMCoreProperties interface [XPS Documents and Packaging]","SetContentType method","IXpsOMCoreProperties.SetContentType","IXpsOMCoreProperties::SetContentType","SetContentType","SetContentType method [XPS Documents and Packaging]","SetContentType method [XPS Documents and Packaging]","IXpsOMCoreProperties interface","xps.ixpsomcoreproperties_setcontenttype","xpsobjectmodel/IXpsOMCoreProperties::SetContentType"]
old-location: xps\ixpsomcoreproperties_setcontenttype.htm
tech.root: xps
ms.assetid: 97ddb1a2-67b2-4891-86b6-bdd38e609229
ms.date: 12/05/2018
ms.keywords: IXpsOMCoreProperties interface [XPS Documents and Packaging],SetContentType method, IXpsOMCoreProperties.SetContentType, IXpsOMCoreProperties::SetContentType, SetContentType, SetContentType method [XPS Documents and Packaging], SetContentType method [XPS Documents and Packaging],IXpsOMCoreProperties interface, xps.ixpsomcoreproperties_setcontenttype, xpsobjectmodel/IXpsOMCoreProperties::SetContentType
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
 - IXpsOMCoreProperties::SetContentType
 - xpsobjectmodel/IXpsOMCoreProperties::SetContentType
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
 - IXpsOMCoreProperties.SetContentType
---

# IXpsOMCoreProperties::SetContentType


## -description

Sets the <b>contentType</b> property.

## -parameters

### -param contentType [in]

The string to be written to the <b>contentType</b> property. A <b>NULL</b> pointer clears the <b>contentType</b> property.

## -returns

If the method succeeds, it returns S_OK; otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The <b>contentType</b> property contains the type of content that is being represented, which is generally defined by a
specific use and intended audience. Examples of <b>contentType</b>  values include <b>Whitepaper</b>, <b>Security Bulletin</b>, and <b>Exam</b>.

## -see-also

<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcoreproperties">IXpsOMCoreProperties</a>



<a href="https://www.ecma-international.org/publications/standards/Ecma-376.htm">Standard ECMA-376, Office Open XML File Formats</a>



<a href="https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf">XML Paper Specification</a>