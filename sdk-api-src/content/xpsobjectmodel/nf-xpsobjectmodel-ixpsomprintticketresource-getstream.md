---
UID: NF:xpsobjectmodel.IXpsOMPrintTicketResource.GetStream
title: IXpsOMPrintTicketResource::GetStream (xpsobjectmodel.h)
description: Gets a new, read-only copy of the stream that is associated with this resource. (IXpsOMPrintTicketResource.GetStream)
helpviewer_keywords: ["GetStream","GetStream method [XPS Documents and Packaging]","GetStream method [XPS Documents and Packaging]","IXpsOMPrintTicketResource interface","IXpsOMPrintTicketResource interface [XPS Documents and Packaging]","GetStream method","IXpsOMPrintTicketResource.GetStream","IXpsOMPrintTicketResource::GetStream","xps.ixpsomprintticketresource_getstream","xpsobjectmodel/IXpsOMPrintTicketResource::GetStream"]
old-location: xps\ixpsomprintticketresource_getstream.htm
tech.root: xps
ms.assetid: 0783cdda-84c6-4441-accf-10fc2610199b
ms.date: 12/05/2018
ms.keywords: GetStream, GetStream method [XPS Documents and Packaging], GetStream method [XPS Documents and Packaging],IXpsOMPrintTicketResource interface, IXpsOMPrintTicketResource interface [XPS Documents and Packaging],GetStream method, IXpsOMPrintTicketResource.GetStream, IXpsOMPrintTicketResource::GetStream, xps.ixpsomprintticketresource_getstream, xpsobjectmodel/IXpsOMPrintTicketResource::GetStream
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
 - IXpsOMPrintTicketResource::GetStream
 - xpsobjectmodel/IXpsOMPrintTicketResource::GetStream
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
 - IXpsOMPrintTicketResource.GetStream
---

# IXpsOMPrintTicketResource::GetStream


## -description

Gets a new, read-only copy of the stream that is associated with this resource.

## -parameters

### -param stream [out, retval]

A new, read-only copy of the stream that is associated with this resource.

## -returns

If the method succeeds, it returns S_OK; otherwise, it returns an <b>HRESULT</b> error code. For information about  XPS document API return values, see <a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>.

This method calls the <a href="/previous-versions/windows/desktop/opc/packaging">Packaging</a> API. For information about the Packaging API return values, see <a href="/previous-versions/windows/desktop/opc/packaging-errors">Packaging Errors</a>.

## -remarks

The <a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream</a> object returned by this method might return an error of E_PENDING, which indicates that the stream length has not been determined yet.  This behavior is different from that of a standard <b>IStream</b> object.

This method calls the stream's <b>Clone</b> method to create the stream returned in <i>stream</i>. As a result, the performance of this method will depend on that of the stream's <b>Clone</b> method.

## -see-also

<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomprintticketresource">IXpsOMPrintTicketResource</a>



<a href="/previous-versions/windows/desktop/opc/packaging-errors">Packaging Errors</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>
