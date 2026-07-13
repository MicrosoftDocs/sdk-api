---
UID: NF:xpsobjectmodel.IXpsOMCoreProperties.SetContentStatus
title: IXpsOMCoreProperties::SetContentStatus (xpsobjectmodel.h)
description: Sets the contentStatus property.
helpviewer_keywords: ["IXpsOMCoreProperties interface [XPS Documents and Packaging]","SetContentStatus method","IXpsOMCoreProperties.SetContentStatus","IXpsOMCoreProperties::SetContentStatus","SetContentStatus","SetContentStatus method [XPS Documents and Packaging]","SetContentStatus method [XPS Documents and Packaging]","IXpsOMCoreProperties interface","xps.ixpsomcoreproperties_setcontentstatus","xpsobjectmodel/IXpsOMCoreProperties::SetContentStatus"]
old-location: xps\ixpsomcoreproperties_setcontentstatus.htm
tech.root: xps
ms.assetid: f500407d-3eb4-4bf1-88ef-8f6bd2bcf472
ms.date: 12/05/2018
ms.keywords: IXpsOMCoreProperties interface [XPS Documents and Packaging],SetContentStatus method, IXpsOMCoreProperties.SetContentStatus, IXpsOMCoreProperties::SetContentStatus, SetContentStatus, SetContentStatus method [XPS Documents and Packaging], SetContentStatus method [XPS Documents and Packaging],IXpsOMCoreProperties interface, xps.ixpsomcoreproperties_setcontentstatus, xpsobjectmodel/IXpsOMCoreProperties::SetContentStatus
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
 - IXpsOMCoreProperties::SetContentStatus
 - xpsobjectmodel/IXpsOMCoreProperties::SetContentStatus
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
 - IXpsOMCoreProperties.SetContentStatus
---

# IXpsOMCoreProperties::SetContentStatus


## -description

Sets the <b>contentStatus</b> property.

## -parameters

### -param contentStatus [in]

The string to be written to the <b>contentStatus</b> property. A <b>NULL</b> pointer clears the <b>contentStatus</b> property.

## -returns

If the method succeeds, it returns S_OK; otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The <b>contentStatus</b> property contains the status of the content. Examples of <b>contentStatus</b> values include <b>Draft</b>, <b>Reviewed</b>, and <b>Final</b>.

## -see-also

<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcoreproperties">IXpsOMCoreProperties</a>



<a href="https://www.ecma-international.org/publications-and-standards/standards/ecma-376/">Standard ECMA-376, Office Open XML File Formats</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>