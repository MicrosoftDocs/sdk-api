---
UID: NF:xpsobjectmodel.IXpsOMCoreProperties.SetLastModifiedBy
title: IXpsOMCoreProperties::SetLastModifiedBy (xpsobjectmodel.h)
description: Sets the lastModifiedBy property.
helpviewer_keywords: ["IXpsOMCoreProperties interface [XPS Documents and Packaging]","SetLastModifiedBy method","IXpsOMCoreProperties.SetLastModifiedBy","IXpsOMCoreProperties::SetLastModifiedBy","SetLastModifiedBy","SetLastModifiedBy method [XPS Documents and Packaging]","SetLastModifiedBy method [XPS Documents and Packaging]","IXpsOMCoreProperties interface","xps.ixpsomcoreproperties_setlastmodifiedby","xpsobjectmodel/IXpsOMCoreProperties::SetLastModifiedBy"]
old-location: xps\ixpsomcoreproperties_setlastmodifiedby.htm
tech.root: xps
ms.assetid: 4c19e7c8-d790-42b8-a0c4-bfd95c7de2c5
ms.date: 12/05/2018
ms.keywords: IXpsOMCoreProperties interface [XPS Documents and Packaging],SetLastModifiedBy method, IXpsOMCoreProperties.SetLastModifiedBy, IXpsOMCoreProperties::SetLastModifiedBy, SetLastModifiedBy, SetLastModifiedBy method [XPS Documents and Packaging], SetLastModifiedBy method [XPS Documents and Packaging],IXpsOMCoreProperties interface, xps.ixpsomcoreproperties_setlastmodifiedby, xpsobjectmodel/IXpsOMCoreProperties::SetLastModifiedBy
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
 - IXpsOMCoreProperties::SetLastModifiedBy
 - xpsobjectmodel/IXpsOMCoreProperties::SetLastModifiedBy
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
 - IXpsOMCoreProperties.SetLastModifiedBy
---

# IXpsOMCoreProperties::SetLastModifiedBy


## -description

Sets the <b>lastModifiedBy</b> property.

## -parameters

### -param lastModifiedBy [in]

The string that contains the value to be written to the <b>lastModifiedBy</b> property. A <b>NULL</b> pointer clears the <b>lastModifiedBy</b> property.

## -returns

If the method succeeds, it returns S_OK; otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The <b>lastModifiedBy</b> property describes the user who performs the last modification.

## -see-also

<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcoreproperties">IXpsOMCoreProperties</a>



<a href="https://www.ecma-international.org/publications-and-standards/standards/ecma-376/">Standard ECMA-376, Office Open XML File Formats</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>