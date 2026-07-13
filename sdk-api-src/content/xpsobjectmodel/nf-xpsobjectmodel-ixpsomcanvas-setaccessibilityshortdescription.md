---
UID: NF:xpsobjectmodel.IXpsOMCanvas.SetAccessibilityShortDescription
title: IXpsOMCanvas::SetAccessibilityShortDescription (xpsobjectmodel.h)
description: Sets the short textual description of the object's contents. (IXpsOMCanvas.SetAccessibilityShortDescription)
helpviewer_keywords: ["IXpsOMCanvas interface [XPS Documents and Packaging]","SetAccessibilityShortDescription method","IXpsOMCanvas.SetAccessibilityShortDescription","IXpsOMCanvas::SetAccessibilityShortDescription","SetAccessibilityShortDescription","SetAccessibilityShortDescription method [XPS Documents and Packaging]","SetAccessibilityShortDescription method [XPS Documents and Packaging]","IXpsOMCanvas interface","xps.ixpsomcanvas_setaccessibilityshortdescription","xpsobjectmodel/IXpsOMCanvas::SetAccessibilityShortDescription"]
old-location: xps\ixpsomcanvas_setaccessibilityshortdescription.htm
tech.root: xps
ms.assetid: 0968e378-99eb-470c-9bf0-51f65906b07b
ms.date: 12/05/2018
ms.keywords: IXpsOMCanvas interface [XPS Documents and Packaging],SetAccessibilityShortDescription method, IXpsOMCanvas.SetAccessibilityShortDescription, IXpsOMCanvas::SetAccessibilityShortDescription, SetAccessibilityShortDescription, SetAccessibilityShortDescription method [XPS Documents and Packaging], SetAccessibilityShortDescription method [XPS Documents and Packaging],IXpsOMCanvas interface, xps.ixpsomcanvas_setaccessibilityshortdescription, xpsobjectmodel/IXpsOMCanvas::SetAccessibilityShortDescription
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
 - IXpsOMCanvas::SetAccessibilityShortDescription
 - xpsobjectmodel/IXpsOMCanvas::SetAccessibilityShortDescription
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
 - IXpsOMCanvas.SetAccessibilityShortDescription
---

# IXpsOMCanvas::SetAccessibilityShortDescription


## -description

Sets the short textual description of the object's contents. This text is used by accessibility clients to describe the object.

## -parameters

### -param shortDescription [in]

The short textual description of the object's contents. A <b>NULL</b> pointer clears the previously assigned text.

## -returns

If the method succeeds, it returns S_OK; otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The property that is set by this method corresponds to the <b>AutomationProperties.HelpText</b> attribute of the <b>Canvas</b> element in the document markup.

## -see-also

<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcanvas">IXpsOMCanvas</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>
