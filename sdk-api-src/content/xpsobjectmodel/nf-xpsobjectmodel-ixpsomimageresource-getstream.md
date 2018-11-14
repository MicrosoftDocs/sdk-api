---
UID: NF:xpsobjectmodel.IXpsOMImageResource.GetStream
title: IXpsOMImageResource::GetStream
author: windows-sdk-content
description: Gets a new, read-only copy of the stream that is associated with this resource.
old-location: xps\ixpsomimageresource_getstream.htm
tech.root: printdocs
ms.assetid: 30d90686-67f5-4e18-811b-472e6a00538f
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: GetStream, GetStream method [XPS Documents and Packaging], GetStream method [XPS Documents and Packaging],IXpsOMImageResource interface, IXpsOMImageResource interface [XPS Documents and Packaging],GetStream method, IXpsOMImageResource.GetStream, IXpsOMImageResource::GetStream, xps.ixpsomimageresource_getstream, xpsobjectmodel/IXpsOMImageResource::GetStream
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IXpsOMImageResource.GetStream
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- xpsobjectmodel.h
: 
- IXpsOMImageResource.GetStream
: 
---

# IXpsOMImageResource::GetStream


## -description


Gets a new, read-only copy of the stream that is associated with this resource.


## -parameters




### -param readerStream [out, retval]

A new, read-only copy of the stream that is associated with this resource.


## -returns



If the method succeeds, it returns S_OK; otherwise, it returns an <b>HRESULT</b> error code. For information about  XPS document API return values, see <a href="https://msdn.microsoft.com/9e6db1e3-7151-4538-8607-b7185ebc0110">XPS Document Errors</a>.

This method calls the <a href="https://msdn.microsoft.com/77df9cb2-757e-4b07-9c1c-73af0df4702f">Packaging</a> API. For information about the Packaging API return values, see <a href="https://msdn.microsoft.com/b4cd8f69-3559-46a0-95ec-6fcaab21959c">Packaging Errors</a>.




## -remarks



The <a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a> object returned by this method might return an error of E_PENDING, which indicates that the stream length has not been determined yet.  This behavior is different from that of a standard <b>IStream</b> object.

This method calls the stream's <b>Clone</b> method to create the stream returned in <i>stream</i>. As a result, the performance of this method will depend on that of the stream's <b>Clone</b> method.




## -see-also




<a href="https://msdn.microsoft.com/89a1530e-fa87-45bf-a1da-c8656ec09ba3">IXpsOMImageResource</a>



<a href="https://msdn.microsoft.com/b4cd8f69-3559-46a0-95ec-6fcaab21959c">Packaging Errors</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://msdn.microsoft.com/9e6db1e3-7151-4538-8607-b7185ebc0110">XPS Document Errors</a>
 

 

