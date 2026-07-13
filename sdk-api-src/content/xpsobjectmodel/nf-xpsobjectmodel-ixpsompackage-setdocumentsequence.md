---
UID: NF:xpsobjectmodel.IXpsOMPackage.SetDocumentSequence
title: IXpsOMPackage::SetDocumentSequence (xpsobjectmodel.h)
description: Sets the IXpsOMDocumentSequence interface of the XPS package.
helpviewer_keywords: ["IXpsOMPackage interface [XPS Documents and Packaging]","SetDocumentSequence method","IXpsOMPackage.SetDocumentSequence","IXpsOMPackage::SetDocumentSequence","SetDocumentSequence","SetDocumentSequence method [XPS Documents and Packaging]","SetDocumentSequence method [XPS Documents and Packaging]","IXpsOMPackage interface","xps.ixpsompackage_setdocumentsequence","xpsobjectmodel/IXpsOMPackage::SetDocumentSequence"]
old-location: xps\ixpsompackage_setdocumentsequence.htm
tech.root: xps
ms.assetid: cc159b7e-7cce-4f3b-ad0d-ce7b625b61d3
ms.date: 12/05/2018
ms.keywords: IXpsOMPackage interface [XPS Documents and Packaging],SetDocumentSequence method, IXpsOMPackage.SetDocumentSequence, IXpsOMPackage::SetDocumentSequence, SetDocumentSequence, SetDocumentSequence method [XPS Documents and Packaging], SetDocumentSequence method [XPS Documents and Packaging],IXpsOMPackage interface, xps.ixpsompackage_setdocumentsequence, xpsobjectmodel/IXpsOMPackage::SetDocumentSequence
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
 - IXpsOMPackage::SetDocumentSequence
 - xpsobjectmodel/IXpsOMPackage::SetDocumentSequence
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
 - IXpsOMPackage.SetDocumentSequence
---

# IXpsOMPackage::SetDocumentSequence


## -description

Sets the <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentsequence">IXpsOMDocumentSequence</a> interface of the XPS package.

## -parameters

### -param documentSequence [in]

The <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentsequence">IXpsOMDocumentSequence</a> interface pointer to be assigned to the package. This parameter must not be <b>NULL</b>.

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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<i>documentSequence</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>XPS_E_NO_CUSTOM_OBJECTS</b></dt>
</dl>
</td>
<td width="60%">
<i>documentSequence</i> does not point to a recognized interface implementation. Custom implementation of XPS Document API interfaces is not supported.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentsequence">IXpsOMDocumentSequence</a>



<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage">IXpsOMPackage</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>