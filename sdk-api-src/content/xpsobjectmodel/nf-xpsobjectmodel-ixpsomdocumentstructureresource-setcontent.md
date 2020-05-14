---
UID: NF:xpsobjectmodel.IXpsOMDocumentStructureResource.SetContent
title: IXpsOMDocumentStructureResource::SetContent (xpsobjectmodel.h)
description: Sets the read-only stream to be associated with this resource.helpviewer_keywords: ["IXpsOMDocumentStructureResource interface [XPS Documents and Packaging]","SetContent method","IXpsOMDocumentStructureResource.SetContent","IXpsOMDocumentStructureResource::SetContent","SetContent","SetContent method [XPS Documents and Packaging]","SetContent method [XPS Documents and Packaging]","IXpsOMDocumentStructureResource interface","xps.ixpsomdocumentstructureresource_setcontent","xpsobjectmodel/IXpsOMDocumentStructureResource::SetContent"]
old-location: xps\ixpsomdocumentstructureresource_setcontent.htm
tech.root: printdocs
ms.assetid: 0b58e0ca-03e7-43ea-aab2-5ac6cdb15807
ms.date: 12/05/2018
ms.keywords: IXpsOMDocumentStructureResource interface [XPS Documents and Packaging],SetContent method, IXpsOMDocumentStructureResource.SetContent, IXpsOMDocumentStructureResource::SetContent, SetContent, SetContent method [XPS Documents and Packaging], SetContent method [XPS Documents and Packaging],IXpsOMDocumentStructureResource interface, xps.ixpsomdocumentstructureresource_setcontent, xpsobjectmodel/IXpsOMDocumentStructureResource::SetContent
f1_keywords:
- xpsobjectmodel/IXpsOMDocumentStructureResource.SetContent
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- xpsobjectmodel.h
api_name:
- IXpsOMDocumentStructureResource.SetContent
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IXpsOMDocumentStructureResource::SetContent


## -description


Sets the read-only stream to be associated with this resource.


## -parameters




### -param sourceStream [in]

The read-only stream to be associated with this resource.


### -param partName [in]

The part name to be assigned to this resource.


## -returns



If the method succeeds, it returns S_OK; otherwise, it returns an <b>HRESULT</b> error code.




## -remarks



The calling method  should treat this stream as a single-threaded apartment (STA) model object and not re-enter any of the stream interface's methods.

For more information about the content of DocumentStructure part, see the <a href="https://www.microsoft.com/download/details.aspx?id=11816">XML Paper Specification</a>.

Because <a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomdocumentstructureresource-getstream">GetStream</a> gets a clone of  the stream that is set by this method, the provided stream should have an efficient cloning method. A stream with an inefficient cloning method will reduce the performance of <b>GetStream</b>.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcparturi">IOpcPartUri</a>



<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentstructureresource">IXpsOMDocumentStructureResource</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/opc/packaging-errors">Packaging Errors</a>



<a href="https://www.microsoft.com/download/details.aspx?id=11816">XML Paper Specification</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>
 

 

