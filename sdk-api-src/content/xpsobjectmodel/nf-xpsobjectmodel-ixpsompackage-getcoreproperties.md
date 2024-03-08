---
UID: NF:xpsobjectmodel.IXpsOMPackage.GetCoreProperties
title: IXpsOMPackage::GetCoreProperties (xpsobjectmodel.h)
description: Gets a pointer to the IXpsOMCoreProperties interface of the XPS package.
helpviewer_keywords: ["GetCoreProperties","GetCoreProperties method [XPS Documents and Packaging]","GetCoreProperties method [XPS Documents and Packaging]","IXpsOMPackage interface","IXpsOMPackage interface [XPS Documents and Packaging]","GetCoreProperties method","IXpsOMPackage.GetCoreProperties","IXpsOMPackage::GetCoreProperties","xps.ixpsompackage_getcoreproperties","xpsobjectmodel/IXpsOMPackage::GetCoreProperties"]
old-location: xps\ixpsompackage_getcoreproperties.htm
tech.root: xps
ms.assetid: ebe5c8a2-2d6a-4a86-8bf3-1fec1dec68d0
ms.date: 12/05/2018
ms.keywords: GetCoreProperties, GetCoreProperties method [XPS Documents and Packaging], GetCoreProperties method [XPS Documents and Packaging],IXpsOMPackage interface, IXpsOMPackage interface [XPS Documents and Packaging],GetCoreProperties method, IXpsOMPackage.GetCoreProperties, IXpsOMPackage::GetCoreProperties, xps.ixpsompackage_getcoreproperties, xpsobjectmodel/IXpsOMPackage::GetCoreProperties
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
 - IXpsOMPackage::GetCoreProperties
 - xpsobjectmodel/IXpsOMPackage::GetCoreProperties
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
 - IXpsOMPackage.GetCoreProperties
---

# IXpsOMPackage::GetCoreProperties


## -description

Gets a pointer to the  <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcoreproperties">IXpsOMCoreProperties</a> interface of the XPS package.

## -parameters

### -param coreProperties [out, retval]

A pointer to the  <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcoreproperties">IXpsOMCoreProperties</a> interface of the XPS package. If an <b>IXpsOMCoreProperties</b> interface has not been set, a <b>NULL</b> pointer is returned.

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
<i>coreProperties</i> is <b>NULL</b>.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcoreproperties">IXpsOMCoreProperties</a>



<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage">IXpsOMPackage</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>