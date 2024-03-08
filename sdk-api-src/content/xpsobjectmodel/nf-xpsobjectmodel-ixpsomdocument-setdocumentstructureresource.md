---
UID: NF:xpsobjectmodel.IXpsOMDocument.SetDocumentStructureResource
title: IXpsOMDocument::SetDocumentStructureResource (xpsobjectmodel.h)
description: Sets the IXpsOMDocumentStructureResource interface for the document.
helpviewer_keywords: ["IXpsOMDocument interface [XPS Documents and Packaging]","SetDocumentStructureResource method","IXpsOMDocument.SetDocumentStructureResource","IXpsOMDocument::SetDocumentStructureResource","SetDocumentStructureResource","SetDocumentStructureResource method [XPS Documents and Packaging]","SetDocumentStructureResource method [XPS Documents and Packaging]","IXpsOMDocument interface","xps.ixpsomdocument_setdocumentstructureresource","xpsobjectmodel/IXpsOMDocument::SetDocumentStructureResource"]
old-location: xps\ixpsomdocument_setdocumentstructureresource.htm
tech.root: xps
ms.assetid: 86d62b73-b7a7-4470-9e55-f4eab50531d0
ms.date: 12/05/2018
ms.keywords: IXpsOMDocument interface [XPS Documents and Packaging],SetDocumentStructureResource method, IXpsOMDocument.SetDocumentStructureResource, IXpsOMDocument::SetDocumentStructureResource, SetDocumentStructureResource, SetDocumentStructureResource method [XPS Documents and Packaging], SetDocumentStructureResource method [XPS Documents and Packaging],IXpsOMDocument interface, xps.ixpsomdocument_setdocumentstructureresource, xpsobjectmodel/IXpsOMDocument::SetDocumentStructureResource
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
 - IXpsOMDocument::SetDocumentStructureResource
 - xpsobjectmodel/IXpsOMDocument::SetDocumentStructureResource
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
 - IXpsOMDocument.SetDocumentStructureResource
---

# IXpsOMDocument::SetDocumentStructureResource


## -description

Sets the <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentstructureresource">IXpsOMDocumentStructureResource</a> interface for the document.

## -parameters

### -param documentStructureResource [in]

A pointer to the <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentstructureresource">IXpsOMDocumentStructureResource</a> interface to be assigned to the document.
          A <b>NULL</b> pointer releases any previously assigned resource.

## -returns

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the table that follows. For information about  XPS document API return values that are not listed in this table, see <a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>XPS_E_NO_CUSTOM_OBJECTS</b></dt>
</dl>
</td>
<td width="60%">
<i>documentStructureResource</i> does not point to a recognized interface implementation. Custom implementation of XPS Document API interfaces is not supported.

</td>
</tr>
</table>

## -remarks

If the document contains an <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentstructureresource">IXpsOMDocumentStructureResource</a> interface when this method is called, that interface is released before the new <b>IXpsOMDocumentStructureResource</b> interface, which is passed in <i>documentStructureResource</i>, is set.

## -see-also

<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocument">IXpsOMDocument</a>



<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentstructureresource">IXpsOMDocumentStructureResource</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>