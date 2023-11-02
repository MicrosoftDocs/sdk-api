---
UID: NF:xpsobjectmodel.IXpsOMCoreProperties.SetDescription
title: IXpsOMCoreProperties::SetDescription (xpsobjectmodel.h)
description: Sets the description property.
helpviewer_keywords: ["IXpsOMCoreProperties interface [XPS Documents and Packaging]","SetDescription method","IXpsOMCoreProperties.SetDescription","IXpsOMCoreProperties::SetDescription","SetDescription","SetDescription method [XPS Documents and Packaging]","SetDescription method [XPS Documents and Packaging]","IXpsOMCoreProperties interface","xps.ixpsomcoreproperties_setdescription","xpsobjectmodel/IXpsOMCoreProperties::SetDescription"]
old-location: xps\ixpsomcoreproperties_setdescription.htm
tech.root: xps
ms.assetid: 5be76080-0f85-4937-913c-2037740a3e9d
ms.date: 12/05/2018
ms.keywords: IXpsOMCoreProperties interface [XPS Documents and Packaging],SetDescription method, IXpsOMCoreProperties.SetDescription, IXpsOMCoreProperties::SetDescription, SetDescription, SetDescription method [XPS Documents and Packaging], SetDescription method [XPS Documents and Packaging],IXpsOMCoreProperties interface, xps.ixpsomcoreproperties_setdescription, xpsobjectmodel/IXpsOMCoreProperties::SetDescription
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
 - IXpsOMCoreProperties::SetDescription
 - xpsobjectmodel/IXpsOMCoreProperties::SetDescription
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
 - IXpsOMCoreProperties.SetDescription
---

# IXpsOMCoreProperties::SetDescription


## -description

Sets the <b>description</b> property.

## -parameters

### -param description [in]

The string to be written to the <b>description</b> property. A <b>NULL</b> pointer clears this property.

## -returns

If the method succeeds, it returns S_OK; otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The <b>description</b> property explains the  content.

## -see-also

<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcoreproperties">IXpsOMCoreProperties</a>



<a href="https://www.ecma-international.org/publications-and-standards/standards/ecma-376/">Standard ECMA-376, Office Open XML File Formats</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>