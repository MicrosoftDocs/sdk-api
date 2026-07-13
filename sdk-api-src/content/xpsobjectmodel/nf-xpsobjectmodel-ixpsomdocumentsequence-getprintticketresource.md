---
UID: NF:xpsobjectmodel.IXpsOMDocumentSequence.GetPrintTicketResource
title: IXpsOMDocumentSequence::GetPrintTicketResource (xpsobjectmodel.h)
description: Gets the IXpsOMPrintTicketResource interface to the job-level print ticket that is assigned to the document sequence.
helpviewer_keywords: ["GetPrintTicketResource","GetPrintTicketResource method [XPS Documents and Packaging]","GetPrintTicketResource method [XPS Documents and Packaging]","IXpsOMDocumentSequence interface","IXpsOMDocumentSequence interface [XPS Documents and Packaging]","GetPrintTicketResource method","IXpsOMDocumentSequence.GetPrintTicketResource","IXpsOMDocumentSequence::GetPrintTicketResource","xps.ixpsomdocumentsequence_getprintticketresource","xpsobjectmodel/IXpsOMDocumentSequence::GetPrintTicketResource"]
old-location: xps\ixpsomdocumentsequence_getprintticketresource.htm
tech.root: xps
ms.assetid: 0d53d537-8db1-4e39-98e6-8987dbf5fc27
ms.date: 12/05/2018
ms.keywords: GetPrintTicketResource, GetPrintTicketResource method [XPS Documents and Packaging], GetPrintTicketResource method [XPS Documents and Packaging],IXpsOMDocumentSequence interface, IXpsOMDocumentSequence interface [XPS Documents and Packaging],GetPrintTicketResource method, IXpsOMDocumentSequence.GetPrintTicketResource, IXpsOMDocumentSequence::GetPrintTicketResource, xps.ixpsomdocumentsequence_getprintticketresource, xpsobjectmodel/IXpsOMDocumentSequence::GetPrintTicketResource
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
 - IXpsOMDocumentSequence::GetPrintTicketResource
 - xpsobjectmodel/IXpsOMDocumentSequence::GetPrintTicketResource
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
 - IXpsOMDocumentSequence.GetPrintTicketResource
---

# IXpsOMDocumentSequence::GetPrintTicketResource


## -description

Gets the <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomprintticketresource">IXpsOMPrintTicketResource</a> interface to the job-level print ticket that is  assigned to the document sequence.

## -parameters

### -param printTicketResource [out, retval]

A pointer to the <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomprintticketresource">IXpsOMPrintTicketResource</a> interface of the job-level print ticket that is  assigned to the document sequence. If no <b>IXpsOMPrintTicketResource</b> interface has been assigned to the document sequence, a <b>NULL</b> pointer is returned.

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
<i>printTicketResource</i> is <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

After loading and parsing the resource into the XPS OM, this method might return an error that applies to another resource. This occurs because all of the relationships are parsed when a resource is loaded.

## -see-also

<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentsequence">IXpsOMDocumentSequence</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>