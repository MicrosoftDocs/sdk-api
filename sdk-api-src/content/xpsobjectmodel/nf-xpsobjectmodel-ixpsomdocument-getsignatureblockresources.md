---
UID: NF:xpsobjectmodel.IXpsOMDocument.GetSignatureBlockResources
title: IXpsOMDocument::GetSignatureBlockResources (xpsobjectmodel.h)
description: Gets a pointer to the IXpsOMSignatureBlockResourceCollection interface, which refers to a collection of the document's digital signature block resources.
helpviewer_keywords: ["GetSignatureBlockResources","GetSignatureBlockResources method [XPS Documents and Packaging]","GetSignatureBlockResources method [XPS Documents and Packaging]","IXpsOMDocument interface","IXpsOMDocument interface [XPS Documents and Packaging]","GetSignatureBlockResources method","IXpsOMDocument.GetSignatureBlockResources","IXpsOMDocument::GetSignatureBlockResources","xps.ixpsomdocument_getsignatureblockresources","xpsobjectmodel/IXpsOMDocument::GetSignatureBlockResources"]
old-location: xps\ixpsomdocument_getsignatureblockresources.htm
tech.root: xps
ms.assetid: 87be3040-6113-4876-a847-93620207647f
ms.date: 12/05/2018
ms.keywords: GetSignatureBlockResources, GetSignatureBlockResources method [XPS Documents and Packaging], GetSignatureBlockResources method [XPS Documents and Packaging],IXpsOMDocument interface, IXpsOMDocument interface [XPS Documents and Packaging],GetSignatureBlockResources method, IXpsOMDocument.GetSignatureBlockResources, IXpsOMDocument::GetSignatureBlockResources, xps.ixpsomdocument_getsignatureblockresources, xpsobjectmodel/IXpsOMDocument::GetSignatureBlockResources
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
 - IXpsOMDocument::GetSignatureBlockResources
 - xpsobjectmodel/IXpsOMDocument::GetSignatureBlockResources
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
 - IXpsOMDocument.GetSignatureBlockResources
---

# IXpsOMDocument::GetSignatureBlockResources


## -description

Gets a pointer to the <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomsignatureblockresourcecollection">IXpsOMSignatureBlockResourceCollection</a> interface, which refers to a collection of the document's digital signature block resources.

## -parameters

### -param signatureBlockResources [out, retval]

A pointer to the <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomsignatureblockresourcecollection">IXpsOMSignatureBlockResourceCollection</a> interface, which refers to a collection of the document's digital signature block resources. If the document does not contain any signature block resources, the <b>IXpsOMSignatureBlockResourceCollection</b> interface will be empty.

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
<i>signatureBlockResources</i> is <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

After loading and parsing the resource into the XPS OM, this method might return an error that applies to another resource. This occurs because all of the relationships are parsed when a resource is loaded.

## -see-also

<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocument">IXpsOMDocument</a>



<a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>