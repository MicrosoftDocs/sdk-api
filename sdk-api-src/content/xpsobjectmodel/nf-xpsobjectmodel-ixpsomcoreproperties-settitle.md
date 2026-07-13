---
UID: NF:xpsobjectmodel.IXpsOMCoreProperties.SetTitle
title: IXpsOMCoreProperties::SetTitle (xpsobjectmodel.h)
description: Sets the title property.
helpviewer_keywords: ["IXpsOMCoreProperties interface [XPS Documents and Packaging]","SetTitle method","IXpsOMCoreProperties.SetTitle","IXpsOMCoreProperties::SetTitle","SetTitle","SetTitle method [XPS Documents and Packaging]","SetTitle method [XPS Documents and Packaging]","IXpsOMCoreProperties interface","xps.ixpsomcoreproperties_settitle","xpsobjectmodel/IXpsOMCoreProperties::SetTitle"]
old-location: xps\ixpsomcoreproperties_settitle.htm
tech.root: xps
ms.assetid: 55562670-576f-483d-abcf-f69ce279245d
ms.date: 12/05/2018
ms.keywords: IXpsOMCoreProperties interface [XPS Documents and Packaging],SetTitle method, IXpsOMCoreProperties.SetTitle, IXpsOMCoreProperties::SetTitle, SetTitle, SetTitle method [XPS Documents and Packaging], SetTitle method [XPS Documents and Packaging],IXpsOMCoreProperties interface, xps.ixpsomcoreproperties_settitle, xpsobjectmodel/IXpsOMCoreProperties::SetTitle
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
 - IXpsOMCoreProperties::SetTitle
 - xpsobjectmodel/IXpsOMCoreProperties::SetTitle
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
 - IXpsOMCoreProperties.SetTitle
---

# IXpsOMCoreProperties::SetTitle


## -description

Sets the <b>title</b> property.

## -parameters

### -param title [in]

The string to be written to the <b>title</b> property. A <b>NULL</b> pointer clears the <b>title</b> property.

## -returns

If the method succeeds, it returns S_OK; otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The <b>title</b> property contains the name given to the resource.

## -see-also

<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcoreproperties">IXpsOMCoreProperties</a>



<a href="https://www.ecma-international.org/publications-and-standards/standards/ecma-376/">Standard ECMA-376, Office Open XML File Formats</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>