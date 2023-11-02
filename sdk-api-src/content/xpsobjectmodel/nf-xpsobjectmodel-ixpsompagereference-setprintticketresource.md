---
UID: NF:xpsobjectmodel.IXpsOMPageReference.SetPrintTicketResource
title: IXpsOMPageReference::SetPrintTicketResource (xpsobjectmodel.h)
description: Sets the IXpsOMPrintTicketResource interface pointer of the page-level print ticket resource that is to be assigned to the page.
helpviewer_keywords: ["IXpsOMPageReference interface [XPS Documents and Packaging]","SetPrintTicketResource method","IXpsOMPageReference.SetPrintTicketResource","IXpsOMPageReference::SetPrintTicketResource","SetPrintTicketResource","SetPrintTicketResource method [XPS Documents and Packaging]","SetPrintTicketResource method [XPS Documents and Packaging]","IXpsOMPageReference interface","xps.ixpsompagereference_setprintticketresource","xpsobjectmodel/IXpsOMPageReference::SetPrintTicketResource"]
old-location: xps\ixpsompagereference_setprintticketresource.htm
tech.root: xps
ms.assetid: 76594c7d-327d-45a5-8947-c587ada7b758
ms.date: 12/05/2018
ms.keywords: IXpsOMPageReference interface [XPS Documents and Packaging],SetPrintTicketResource method, IXpsOMPageReference.SetPrintTicketResource, IXpsOMPageReference::SetPrintTicketResource, SetPrintTicketResource, SetPrintTicketResource method [XPS Documents and Packaging], SetPrintTicketResource method [XPS Documents and Packaging],IXpsOMPageReference interface, xps.ixpsompagereference_setprintticketresource, xpsobjectmodel/IXpsOMPageReference::SetPrintTicketResource
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
 - IXpsOMPageReference::SetPrintTicketResource
 - xpsobjectmodel/IXpsOMPageReference::SetPrintTicketResource
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
 - IXpsOMPageReference.SetPrintTicketResource
---

# IXpsOMPageReference::SetPrintTicketResource


## -description

Sets  the <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomprintticketresource">IXpsOMPrintTicketResource</a> interface pointer of the page-level print ticket resource that is to be assigned to the page.

## -parameters

### -param printTicketResource [in]

A pointer to the <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomprintticketresource">IXpsOMPrintTicketResource</a> interface of the page-level print ticket resource that is to be assigned to the page. If a print ticket has already been set, a <b>NULL</b> pointer releases it.

## -returns

If the method succeeds, it returns S_OK; otherwise, it returns an <b>HRESULT</b> error code.

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

## -see-also

<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereference">IXpsOMPageReference</a>



<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomprintticketresource">IXpsOMPrintTicketResource</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>