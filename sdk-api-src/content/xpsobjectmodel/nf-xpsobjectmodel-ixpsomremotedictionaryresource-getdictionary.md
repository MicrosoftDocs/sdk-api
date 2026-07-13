---
UID: NF:xpsobjectmodel.IXpsOMRemoteDictionaryResource.GetDictionary
title: IXpsOMRemoteDictionaryResource::GetDictionary (xpsobjectmodel.h)
description: Gets a pointer to the IXpsOMDictionary interface of the remote dictionary that is associated with this resource.
helpviewer_keywords: ["GetDictionary","GetDictionary method [XPS Documents and Packaging]","GetDictionary method [XPS Documents and Packaging]","IXpsOMRemoteDictionaryResource interface","IXpsOMRemoteDictionaryResource interface [XPS Documents and Packaging]","GetDictionary method","IXpsOMRemoteDictionaryResource.GetDictionary","IXpsOMRemoteDictionaryResource::GetDictionary","xps.ixpsomremotedictionaryresource_getdictionary","xpsobjectmodel/IXpsOMRemoteDictionaryResource::GetDictionary"]
old-location: xps\ixpsomremotedictionaryresource_getdictionary.htm
tech.root: xps
ms.assetid: 8363aa97-b7ca-458e-84d9-d9316070a3d0
ms.date: 12/05/2018
ms.keywords: GetDictionary, GetDictionary method [XPS Documents and Packaging], GetDictionary method [XPS Documents and Packaging],IXpsOMRemoteDictionaryResource interface, IXpsOMRemoteDictionaryResource interface [XPS Documents and Packaging],GetDictionary method, IXpsOMRemoteDictionaryResource.GetDictionary, IXpsOMRemoteDictionaryResource::GetDictionary, xps.ixpsomremotedictionaryresource_getdictionary, xpsobjectmodel/IXpsOMRemoteDictionaryResource::GetDictionary
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
 - IXpsOMRemoteDictionaryResource::GetDictionary
 - xpsobjectmodel/IXpsOMRemoteDictionaryResource::GetDictionary
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
 - IXpsOMRemoteDictionaryResource.GetDictionary
---

# IXpsOMRemoteDictionaryResource::GetDictionary


## -description

Gets a pointer to the  <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdictionary">IXpsOMDictionary</a> interface  of the remote dictionary that is associated with this resource.

## -parameters

### -param dictionary [out, retval]

A pointer to the <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdictionary">IXpsOMDictionary</a> interface of the dictionary that is associated with this resource.

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
<i>dictionary</i> is <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

After loading and parsing the resource into the XPS OM, this method might return an error that applies to another resource. This occurs because all of the relationships are parsed when a resource is loaded.

## -see-also

<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomremotedictionaryresource">IXpsOMRemoteDictionaryResource</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>