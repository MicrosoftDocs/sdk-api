---
UID: NL:vswriter.IVssCreateExpressWriterMetadata
title: IVssCreateExpressWriterMetadata (vswriter.h)
description: The IVssCreateExpressWriterMetadata interface is a COM interface containing methods to construct the Writer Metadata Document for an express writer.
helpviewer_keywords: ["IVssCreateExpressWriterMetadata","IVssCreateExpressWriterMetadata interface","IVssCreateExpressWriterMetadata interface","described","base.ivsscreateexpresswritermetadata","vswriter/IVssCreateExpressWriterMetadata"]
old-location: base\ivsscreateexpresswritermetadata.htm
tech.root: base
ms.assetid: 49112cff-9e61-4218-a013-5ae5eb58b534
ms.date: 12/05/2018
ms.keywords: IVssCreateExpressWriterMetadata, IVssCreateExpressWriterMetadata interface, IVssCreateExpressWriterMetadata interface,described, base.ivsscreateexpresswritermetadata, vswriter/IVssCreateExpressWriterMetadata
req.header: vswriter.h
req.include-header: Vss.h, VsWriter.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: VssApi.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IVssCreateExpressWriterMetadata
 - vswriter/IVssCreateExpressWriterMetadata
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - VssApi.lib
 - VssApi.dll
api_name:
 - IVssCreateExpressWriterMetadata
---

# IVssCreateExpressWriterMetadata class


## -description

The <b>IVssCreateExpressWriterMetadata</b> interface is a COM interface containing methods to construct the Writer Metadata Document for an express writer.

After it is constructed, the Writer Metadata Document is a read-only object that requesters query for information about a writer and its components.

## -inheritance

The <b>IVssCreateExpressWriterMetadata</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IVssCreateExpressWriterMetadata</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/vswriter/nl-vswriter-ivsscreatewritermetadata">IVssCreateWriterMetadata</a>



<a href="/windows/desktop/api/vswriter/nl-vswriter-ivssexpresswriter">IVssExpressWriter</a>
