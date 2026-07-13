---
UID: NF:xpsobjectmodel.IXpsOMShareable.GetOwner
title: IXpsOMShareable::GetOwner (xpsobjectmodel.h)
description: Gets the IUnknown interface of the parent.
helpviewer_keywords: ["GetOwner","GetOwner method [XPS Documents and Packaging]","GetOwner method [XPS Documents and Packaging]","IXpsOMShareable interface","IXpsOMShareable interface [XPS Documents and Packaging]","GetOwner method","IXpsOMShareable.GetOwner","IXpsOMShareable::GetOwner","xps.ixpsomshareable_getowner","xpsobjectmodel/IXpsOMShareable::GetOwner"]
old-location: xps\ixpsomshareable_getowner.htm
tech.root: xps
ms.assetid: da871b31-2787-44cc-8678-43d529472f61
ms.date: 12/05/2018
ms.keywords: GetOwner, GetOwner method [XPS Documents and Packaging], GetOwner method [XPS Documents and Packaging],IXpsOMShareable interface, IXpsOMShareable interface [XPS Documents and Packaging],GetOwner method, IXpsOMShareable.GetOwner, IXpsOMShareable::GetOwner, xps.ixpsomshareable_getowner, xpsobjectmodel/IXpsOMShareable::GetOwner
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
 - IXpsOMShareable::GetOwner
 - xpsobjectmodel/IXpsOMShareable::GetOwner
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
 - IXpsOMShareable.GetOwner
---

# IXpsOMShareable::GetOwner


## -description

Gets the <b>IUnknown</b> interface of the parent.

## -parameters

### -param owner [out, retval]

A pointer to the <b>IUnknown</b> interface of the parent.

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
<i>owner</i> is <b>NULL</b>.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomshareable">IXpsOMShareable</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>