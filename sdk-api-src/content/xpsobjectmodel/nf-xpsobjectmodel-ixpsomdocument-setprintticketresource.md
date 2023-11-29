---
UID: NF:xpsobjectmodel.IXpsOMDocument.SetPrintTicketResource
title: IXpsOMDocument::SetPrintTicketResource (xpsobjectmodel.h)
description: Sets the IXpsOMPrintTicketResource interface for the document-level print ticket.
helpviewer_keywords: ["IXpsOMDocument interface [XPS Documents and Packaging]","SetPrintTicketResource method","IXpsOMDocument.SetPrintTicketResource","IXpsOMDocument::SetPrintTicketResource","SetPrintTicketResource","SetPrintTicketResource method [XPS Documents and Packaging]","SetPrintTicketResource method [XPS Documents and Packaging]","IXpsOMDocument interface","xps.ixpsomdocument_setprintticketresource","xpsobjectmodel/IXpsOMDocument::SetPrintTicketResource"]
old-location: xps\ixpsomdocument_setprintticketresource.htm
tech.root: xps
ms.assetid: 009c2124-c855-4043-9a23-c0313b504853
ms.date: 12/05/2018
ms.keywords: IXpsOMDocument interface [XPS Documents and Packaging],SetPrintTicketResource method, IXpsOMDocument.SetPrintTicketResource, IXpsOMDocument::SetPrintTicketResource, SetPrintTicketResource, SetPrintTicketResource method [XPS Documents and Packaging], SetPrintTicketResource method [XPS Documents and Packaging],IXpsOMDocument interface, xps.ixpsomdocument_setprintticketresource, xpsobjectmodel/IXpsOMDocument::SetPrintTicketResource
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
 - IXpsOMDocument::SetPrintTicketResource
 - xpsobjectmodel/IXpsOMDocument::SetPrintTicketResource
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
 - IXpsOMDocument.SetPrintTicketResource
---

# IXpsOMDocument::SetPrintTicketResource


## -description

Sets the <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomprintticketresource">IXpsOMPrintTicketResource</a> interface for the  document-level print ticket.

## -parameters

### -param printTicketResource [in]

A pointer to the <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomprintticketresource">IXpsOMPrintTicketResource</a> interface for the document-level print ticket to be assigned to the document.
          A <b>NULL</b> pointer releases any previously assigned print ticket resource.

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
<i>printTicketResource</i> does not point to a recognized interface implementation. Custom implementation of XPS Document API interfaces is not supported.

</td>
</tr>
</table>

## -remarks

If the document contains an <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomprintticketresource">IXpsOMPrintTicketResource</a> interface when this method is called, that interface is released before the new <b>IXpsOMPrintTicketResource</b> interface, passed in <i>printTicketResource</i>, is set.

## -see-also

<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocument">IXpsOMDocument</a>



<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomprintticketresource">IXpsOMPrintTicketResource</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>