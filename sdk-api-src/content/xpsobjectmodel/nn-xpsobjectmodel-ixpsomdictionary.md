---
UID: NN:xpsobjectmodel.IXpsOMDictionary
title: IXpsOMDictionary (xpsobjectmodel.h)
description: The dictionary is used by an XPS package to share resources.
helpviewer_keywords: ["IXpsOMDictionary","IXpsOMDictionary interface [XPS Documents and Packaging]","IXpsOMDictionary interface [XPS Documents and Packaging]","described","xps.ixpsomdictionary","xpsobjectmodel/IXpsOMDictionary"]
old-location: xps\ixpsomdictionary.htm
tech.root: xps
ms.assetid: f887e3d3-973c-4267-a785-6bc190c13082
ms.date: 12/05/2018
ms.keywords: IXpsOMDictionary, IXpsOMDictionary interface [XPS Documents and Packaging], IXpsOMDictionary interface [XPS Documents and Packaging],described, xps.ixpsomdictionary, xpsobjectmodel/IXpsOMDictionary
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
 - IXpsOMDictionary
 - xpsobjectmodel/IXpsOMDictionary
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
 - IXpsOMDictionary
---

# IXpsOMDictionary interface

## -description

The dictionary is used by an XPS package to share resources.

## -inheritance

The <b>IXpsOMDictionary</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IXpsOMDictionary</b> also has these types of members:

## -remarks

The interface pointers stored in a dictionary will usually point to interfaces, such as <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsombrush">IXpsOMBrush</a>                 and <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisual">IXpsOMVisual</a>, that are derived from the <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomshareable">IXpsOMShareable</a> interface. To determine the interface type, call the <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomshareable-gettype">IXpsOMShareable::GetType</a> method.

A dictionary cannot contain duplicate interface pointers.

## -see-also

<a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createdictionary">IXpsOMObjectFactory::CreateDictionary</a>



<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomshareable">IXpsOMShareable</a>



<a href="/previous-versions/windows/desktop/dd316980(v=vs.85)">Interfaces</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>
