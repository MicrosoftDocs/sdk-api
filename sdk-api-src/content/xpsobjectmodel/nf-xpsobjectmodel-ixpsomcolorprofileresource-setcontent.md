---
UID: NF:xpsobjectmodel.IXpsOMColorProfileResource.SetContent
title: IXpsOMColorProfileResource::SetContent (xpsobjectmodel.h)
description: Sets the read-only stream to be associated with this resource. (IXpsOMColorProfileResource.SetContent)
helpviewer_keywords: ["IXpsOMColorProfileResource interface [XPS Documents and Packaging]","SetContent method","IXpsOMColorProfileResource.SetContent","IXpsOMColorProfileResource::SetContent","SetContent","SetContent method [XPS Documents and Packaging]","SetContent method [XPS Documents and Packaging]","IXpsOMColorProfileResource interface","xps.ixpsomcolorprofileresource_setcontent","xpsobjectmodel/IXpsOMColorProfileResource::SetContent"]
old-location: xps\ixpsomcolorprofileresource_setcontent.htm
tech.root: xps
ms.assetid: d93ae074-6565-45ea-bc0e-e8401b7d5b47
ms.date: 12/05/2018
ms.keywords: IXpsOMColorProfileResource interface [XPS Documents and Packaging],SetContent method, IXpsOMColorProfileResource.SetContent, IXpsOMColorProfileResource::SetContent, SetContent, SetContent method [XPS Documents and Packaging], SetContent method [XPS Documents and Packaging],IXpsOMColorProfileResource interface, xps.ixpsomcolorprofileresource_setcontent, xpsobjectmodel/IXpsOMColorProfileResource::SetContent
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
 - IXpsOMColorProfileResource::SetContent
 - xpsobjectmodel/IXpsOMColorProfileResource::SetContent
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
 - IXpsOMColorProfileResource.SetContent
---

# IXpsOMColorProfileResource::SetContent


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

Because <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomcolorprofileresource-getstream">GetStream</a> gets a clone of  the stream that is set by this method, the provided stream should have an efficient cloning method. A stream with an inefficient cloning method will reduce the performance of <b>GetStream</b>.

## -see-also

<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcparturi">IOpcPartUri</a>



<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcolorprofileresource">IXpsOMColorProfileResource</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>
