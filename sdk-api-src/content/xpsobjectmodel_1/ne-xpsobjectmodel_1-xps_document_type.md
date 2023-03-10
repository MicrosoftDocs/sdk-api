---
UID: NE:xpsobjectmodel_1.__MIDL___MIDL_itf_xpsobjectmodel_1_0000_0000_0001
title: XPS_DOCUMENT_TYPE (xpsobjectmodel_1.h)
description: Indicates the format into which the document was serialized.
helpviewer_keywords: ["XPS_DOCUMENT_TYPE","XPS_DOCUMENT_TYPE enumeration [XPS Documents and Packaging]","XPS_DOCUMENT_TYPE_OPENXPS","XPS_DOCUMENT_TYPE_UNSPECIFIED","XPS_DOCUMENT_TYPE_XPS","xps.xps_document_type","xpsobjectmodel_1/XPS_DOCUMENT_TYPE","xpsobjectmodel_1/XPS_DOCUMENT_TYPE_OPENXPS","xpsobjectmodel_1/XPS_DOCUMENT_TYPE_UNSPECIFIED","xpsobjectmodel_1/XPS_DOCUMENT_TYPE_XPS"]
old-location: xps\xps_document_type.htm
tech.root: xps
ms.assetid: C34629CB-7F8C-4126-BBE3-BF506D7586E9
ms.date: 12/05/2018
ms.keywords: XPS_DOCUMENT_TYPE, XPS_DOCUMENT_TYPE enumeration [XPS Documents and Packaging], XPS_DOCUMENT_TYPE_OPENXPS, XPS_DOCUMENT_TYPE_UNSPECIFIED, XPS_DOCUMENT_TYPE_XPS, xps.xps_document_type, xpsobjectmodel_1/XPS_DOCUMENT_TYPE, xpsobjectmodel_1/XPS_DOCUMENT_TYPE_OPENXPS, xpsobjectmodel_1/XPS_DOCUMENT_TYPE_UNSPECIFIED, xpsobjectmodel_1/XPS_DOCUMENT_TYPE_XPS
req.header: xpsobjectmodel_1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Xpsobjectmodel_1.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: XPS_DOCUMENT_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL___MIDL_itf_xpsobjectmodel_1_0000_0000_0001
 - xpsobjectmodel_1/__MIDL___MIDL_itf_xpsobjectmodel_1_0000_0000_0001
 - XPS_DOCUMENT_TYPE
 - xpsobjectmodel_1/XPS_DOCUMENT_TYPE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - xpsobjectmodel_1.h
api_name:
 - XPS_DOCUMENT_TYPE
---

# XPS_DOCUMENT_TYPE enumeration


## -description

Indicates the format into which the document was serialized.

## -enum-fields

### -field XPS_DOCUMENT_TYPE_UNSPECIFIED:1

For documents which have yet to be serialized, and whose type is yet to be determined.

### -field XPS_DOCUMENT_TYPE_XPS

MSXPS v1.0 document format.

### -field XPS_DOCUMENT_TYPE_OPENXPS

OpenXPS v1.0 document format.

## -see-also

<a href="/windows/desktop/api/xpsobjectmodel_1/nf-xpsobjectmodel_1-ixpsdocumentpackagetarget-getxpstype">IXpsDocumentPackageTarget::GetXpsType</a>



<a href="/previous-versions/windows/desktop/dd316978(v=vs.85)">XPS Document Enumerations</a>
