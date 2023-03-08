---
UID: NF:xpsobjectmodel.IXpsOMCoreProperties.SetIdentifier
title: IXpsOMCoreProperties::SetIdentifier (xpsobjectmodel.h)
description: Sets the identifier property.
helpviewer_keywords: ["IXpsOMCoreProperties interface [XPS Documents and Packaging]","SetIdentifier method","IXpsOMCoreProperties.SetIdentifier","IXpsOMCoreProperties::SetIdentifier","SetIdentifier","SetIdentifier method [XPS Documents and Packaging]","SetIdentifier method [XPS Documents and Packaging]","IXpsOMCoreProperties interface","xps.ixpsomcoreproperties_setidentifier","xpsobjectmodel/IXpsOMCoreProperties::SetIdentifier"]
old-location: xps\ixpsomcoreproperties_setidentifier.htm
tech.root: xps
ms.assetid: 8ad5a359-77f6-4b11-9c1c-2e4094be65d0
ms.date: 12/05/2018
ms.keywords: IXpsOMCoreProperties interface [XPS Documents and Packaging],SetIdentifier method, IXpsOMCoreProperties.SetIdentifier, IXpsOMCoreProperties::SetIdentifier, SetIdentifier, SetIdentifier method [XPS Documents and Packaging], SetIdentifier method [XPS Documents and Packaging],IXpsOMCoreProperties interface, xps.ixpsomcoreproperties_setidentifier, xpsobjectmodel/IXpsOMCoreProperties::SetIdentifier
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
 - IXpsOMCoreProperties::SetIdentifier
 - xpsobjectmodel/IXpsOMCoreProperties::SetIdentifier
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
 - IXpsOMCoreProperties.SetIdentifier
---

# IXpsOMCoreProperties::SetIdentifier


## -description

Sets the <b>identifier</b> property.

## -parameters

### -param identifier [in]

The string to be written to the <b>identifier</b> property. A <b>NULL</b> pointer clears the <b>identifier</b> property.

## -returns

If the method succeeds, it returns S_OK; otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The <b>identifier</b> property is an unambiguous reference to the resource within a user-defined or application-specific
context.

## -see-also

<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcoreproperties">IXpsOMCoreProperties</a>



<a href="https://www.ecma-international.org/publications/standards/Ecma-376.htm">Standard ECMA-376, Office Open XML File Formats</a>



<a href="https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf">XML Paper Specification</a>