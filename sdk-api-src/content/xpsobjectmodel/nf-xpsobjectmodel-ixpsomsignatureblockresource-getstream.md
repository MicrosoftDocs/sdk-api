---
UID: NF:xpsobjectmodel.IXpsOMSignatureBlockResource.GetStream
title: IXpsOMSignatureBlockResource::GetStream (xpsobjectmodel.h)
author: windows-sdk-content
description: Gets a new, read-only copy of the stream that is associated with this resource.
old-location: xps\ixpsomsignatureblockresource_getstream.htm
tech.root: printdocs
ms.assetid: 1e6c53fa-7180-454d-8bdc-332eb0d3fa27
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetStream, GetStream method [XPS Documents and Packaging], GetStream method [XPS Documents and Packaging],IXpsOMSignatureBlockResource interface, IXpsOMSignatureBlockResource interface [XPS Documents and Packaging],GetStream method, IXpsOMSignatureBlockResource.GetStream, IXpsOMSignatureBlockResource::GetStream, xps.ixpsomsignatureblockresource_getstream, xpsobjectmodel/IXpsOMSignatureBlockResource::GetStream
ms.topic: method
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
 - IXpsOMSignatureBlockResource.GetStream
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IXpsOMSignatureBlockResource::GetStream


## -description


Gets a new, read-only copy of the stream that is associated with this resource.


## -parameters




### -param stream [out, retval]

A new, read-only copy of the stream that is associated with this resource.


## -returns



If the method succeeds, it returns S_OK; otherwise, it returns an <b>HRESULT</b> error code. For information about  XPS document API return values, see <a href="https://docs.microsoft.com/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>.

This method calls the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/opc/packaging">Packaging</a> API. For information about the Packaging API return values, see <a href="https://docs.microsoft.com/previous-versions/windows/desktop/opc/packaging-errors">Packaging Errors</a>.




## -remarks



The <a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-istream">IStream</a> object returned by this method might return an error of E_PENDING, which indicates that the stream length has not been determined yet.  This behavior is different from that of a standard <b>IStream</b> object.

This method calls the stream's <b>Clone</b> method to create the stream returned in <i>stream</i>. As a result, the performance of this method will depend on that of the stream's <b>Clone</b> method.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomsignatureblockresource">IXpsOMSignatureBlockResource</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/opc/packaging-errors">Packaging Errors</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>
 

 

