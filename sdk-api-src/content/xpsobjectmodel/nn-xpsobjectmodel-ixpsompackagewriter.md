---
UID: NN:xpsobjectmodel.IXpsOMPackageWriter
title: IXpsOMPackageWriter (xpsobjectmodel.h)
description: Incrementally writes the parts of an XPS document to a package file.
helpviewer_keywords: ["IXpsOMPackageWriter","IXpsOMPackageWriter interface [XPS Documents and Packaging]","IXpsOMPackageWriter interface [XPS Documents and Packaging]","described","xps.ixpsompackagewriter","xpsobjectmodel/IXpsOMPackageWriter"]
old-location: xps\ixpsompackagewriter.htm
tech.root: xps
ms.assetid: cbbcc8bf-6172-41c8-9d74-27e5635ec167
ms.date: 12/05/2018
ms.keywords: IXpsOMPackageWriter, IXpsOMPackageWriter interface [XPS Documents and Packaging], IXpsOMPackageWriter interface [XPS Documents and Packaging],described, xps.ixpsompackagewriter, xpsobjectmodel/IXpsOMPackageWriter
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
 - IXpsOMPackageWriter
 - xpsobjectmodel/IXpsOMPackageWriter
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
 - IXpsOMPackageWriter
---

# IXpsOMPackageWriter interface

## -description

Incrementally writes the parts of an XPS document to  a package file.

## -inheritance

The <b>IXpsOMPackageWriter</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IXpsOMPackageWriter</b> also has these types of members:

## -remarks

Progressive writing enables an application to serialize  XPS document content and resources as they become available. It does not require the application to create all elements of the document before serialization.

This interface writes the pages to the package sequentially, in the order that  <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackagewriter-addpage">AddPage</a> is called. The interface does not support page writing in a non-sequential order; thus it should only be used when page content is produced or is available for writing in the order it is to appear in the XPS document.

## -see-also

<a href="/windows/desktop/api/xpsobjectmodel_1/nf-xpsobjectmodel_1-ixpsdocumentpackagetarget-getxpsompackagewriter">IXpsDocumentPackageTarget::GetXpsOMPackageWriter</a>



<a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createpackagewriteronfile">IXpsOMObjectFactory::CreatePackageWriterOnFile</a>



<a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createpackagewriteronstream">IXpsOMObjectFactory::CreatePackageWriterOnStream</a>



<a href="/previous-versions/windows/desktop/dd372920(v=vs.85)">Print an XPS OM</a>



<a href="/previous-versions/windows/desktop/dd464658(v=vs.85)">Using the IXpsOMPackageWriter Interface</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>
