---
UID: NF:xpsobjectmodel.IXpsOMDocumentSequence.SetPrintTicketResource
title: IXpsOMDocumentSequence::SetPrintTicketResource (xpsobjectmodel.h)
description: Sets the job-level print ticket resource for the document sequence.
helpviewer_keywords: ["IXpsOMDocumentSequence interface [XPS Documents and Packaging]","SetPrintTicketResource method","IXpsOMDocumentSequence.SetPrintTicketResource","IXpsOMDocumentSequence::SetPrintTicketResource","SetPrintTicketResource","SetPrintTicketResource method [XPS Documents and Packaging]","SetPrintTicketResource method [XPS Documents and Packaging]","IXpsOMDocumentSequence interface","xps.ixpsomdocumentsequence_setprintticketresource","xpsobjectmodel/IXpsOMDocumentSequence::SetPrintTicketResource"]
old-location: xps\ixpsomdocumentsequence_setprintticketresource.htm
tech.root: xps
ms.assetid: bfc5889d-ab1d-4dbe-af11-625ee5e8c95f
ms.date: 12/05/2018
ms.keywords: IXpsOMDocumentSequence interface [XPS Documents and Packaging],SetPrintTicketResource method, IXpsOMDocumentSequence.SetPrintTicketResource, IXpsOMDocumentSequence::SetPrintTicketResource, SetPrintTicketResource, SetPrintTicketResource method [XPS Documents and Packaging], SetPrintTicketResource method [XPS Documents and Packaging],IXpsOMDocumentSequence interface, xps.ixpsomdocumentsequence_setprintticketresource, xpsobjectmodel/IXpsOMDocumentSequence::SetPrintTicketResource
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
 - IXpsOMDocumentSequence::SetPrintTicketResource
 - xpsobjectmodel/IXpsOMDocumentSequence::SetPrintTicketResource
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
 - IXpsOMDocumentSequence.SetPrintTicketResource
---

# IXpsOMDocumentSequence::SetPrintTicketResource


## -description

Sets the job-level print ticket resource for the document sequence.

## -parameters

### -param printTicketResource [in]

A pointer to the  <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomprintticketresource">IXpsOMPrintTicketResource</a> interface of the job-level print ticket that will be set for the document sequence.
          If the document sequence has a print ticket resource, a <b>NULL</b> pointer will release it.

## -returns

If the method succeeds, it returns S_OK; otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

If the document contains an <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomprintticketresource">IXpsOMPrintTicketResource</a> interface when this method is called, that interface is released before the new <b>IXpsOMPrintTicketResource</b> interface, which is passed in <i>printTicketResource</i>, is set.

## -see-also

<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentsequence">IXpsOMDocumentSequence</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>