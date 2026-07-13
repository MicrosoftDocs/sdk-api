---
UID: NF:xpsobjectmodel.IXpsOMCoreProperties.SetCategory
title: IXpsOMCoreProperties::SetCategory (xpsobjectmodel.h)
description: Sets the category property.
helpviewer_keywords: ["IXpsOMCoreProperties interface [XPS Documents and Packaging]","SetCategory method","IXpsOMCoreProperties.SetCategory","IXpsOMCoreProperties::SetCategory","SetCategory","SetCategory method [XPS Documents and Packaging]","SetCategory method [XPS Documents and Packaging]","IXpsOMCoreProperties interface","xps.ixpsomcoreproperties_setcategory","xpsobjectmodel/IXpsOMCoreProperties::SetCategory"]
old-location: xps\ixpsomcoreproperties_setcategory.htm
tech.root: xps
ms.assetid: 0c194731-0992-47c3-b069-fa9e1d16944b
ms.date: 12/05/2018
ms.keywords: IXpsOMCoreProperties interface [XPS Documents and Packaging],SetCategory method, IXpsOMCoreProperties.SetCategory, IXpsOMCoreProperties::SetCategory, SetCategory, SetCategory method [XPS Documents and Packaging], SetCategory method [XPS Documents and Packaging],IXpsOMCoreProperties interface, xps.ixpsomcoreproperties_setcategory, xpsobjectmodel/IXpsOMCoreProperties::SetCategory
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
 - IXpsOMCoreProperties::SetCategory
 - xpsobjectmodel/IXpsOMCoreProperties::SetCategory
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
 - IXpsOMCoreProperties.SetCategory
---

# IXpsOMCoreProperties::SetCategory


## -description

Sets the <b>category</b> property.

## -parameters

### -param category [in]

The string to be written to the <b>category</b> property. A <b>NULL</b> pointer clears the <b>category</b> property.

## -returns

If the method succeeds, it returns S_OK; otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The <b>category</b> property contains a categorization of the content.

## -see-also

<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcoreproperties">IXpsOMCoreProperties</a>



<a href="https://www.ecma-international.org/publications-and-standards/standards/ecma-376/">Standard ECMA-376, Office Open XML File Formats</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>