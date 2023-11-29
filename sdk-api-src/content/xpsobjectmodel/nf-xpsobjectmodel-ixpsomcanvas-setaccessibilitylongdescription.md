---
UID: NF:xpsobjectmodel.IXpsOMCanvas.SetAccessibilityLongDescription
title: IXpsOMCanvas::SetAccessibilityLongDescription (xpsobjectmodel.h)
description: Sets the long (detailed) textual description of the object's contents. (IXpsOMCanvas.SetAccessibilityLongDescription)
helpviewer_keywords: ["IXpsOMCanvas interface [XPS Documents and Packaging]","SetAccessibilityLongDescription method","IXpsOMCanvas.SetAccessibilityLongDescription","IXpsOMCanvas::SetAccessibilityLongDescription","SetAccessibilityLongDescription","SetAccessibilityLongDescription method [XPS Documents and Packaging]","SetAccessibilityLongDescription method [XPS Documents and Packaging]","IXpsOMCanvas interface","xps.ixpsomcanvas_setaccessibilitylongdescription","xpsobjectmodel/IXpsOMCanvas::SetAccessibilityLongDescription"]
old-location: xps\ixpsomcanvas_setaccessibilitylongdescription.htm
tech.root: xps
ms.assetid: 1b9da720-2823-4749-b881-3b9cd5c303a4
ms.date: 12/05/2018
ms.keywords: IXpsOMCanvas interface [XPS Documents and Packaging],SetAccessibilityLongDescription method, IXpsOMCanvas.SetAccessibilityLongDescription, IXpsOMCanvas::SetAccessibilityLongDescription, SetAccessibilityLongDescription, SetAccessibilityLongDescription method [XPS Documents and Packaging], SetAccessibilityLongDescription method [XPS Documents and Packaging],IXpsOMCanvas interface, xps.ixpsomcanvas_setaccessibilitylongdescription, xpsobjectmodel/IXpsOMCanvas::SetAccessibilityLongDescription
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
 - IXpsOMCanvas::SetAccessibilityLongDescription
 - xpsobjectmodel/IXpsOMCanvas::SetAccessibilityLongDescription
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
 - IXpsOMCanvas.SetAccessibilityLongDescription
---

# IXpsOMCanvas::SetAccessibilityLongDescription


## -description

Sets the long (detailed) textual description of the object's contents. This text is used by accessibility clients to describe the object.

## -parameters

### -param longDescription [in]

The long (detailed) textual description of the object's contents. A <b>NULL</b> pointer clears the previously assigned value.

## -returns

If the method succeeds, it returns S_OK; otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The property that is set by this method corresponds to the <b>AutomationProperties.HelpText</b> attribute of the <b>Canvas</b> element in the document markup.

## -see-also

<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcanvas">IXpsOMCanvas</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>
