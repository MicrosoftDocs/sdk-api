---
UID: NF:xpsobjectmodel.IXpsOMRemoteDictionaryResource.SetDictionary
title: IXpsOMRemoteDictionaryResource::SetDictionary (xpsobjectmodel.h)
description: Sets a pointer to the IXpsOMDictionary interface of the remote dictionary that is to be associated with this resource.
helpviewer_keywords: ["IXpsOMRemoteDictionaryResource interface [XPS Documents and Packaging]","SetDictionary method","IXpsOMRemoteDictionaryResource.SetDictionary","IXpsOMRemoteDictionaryResource::SetDictionary","SetDictionary","SetDictionary method [XPS Documents and Packaging]","SetDictionary method [XPS Documents and Packaging]","IXpsOMRemoteDictionaryResource interface","xps.ixpsomremotedictionaryresource_setdictionary","xpsobjectmodel/IXpsOMRemoteDictionaryResource::SetDictionary"]
old-location: xps\ixpsomremotedictionaryresource_setdictionary.htm
tech.root: xps
ms.assetid: 68aba55b-d755-4ed3-8ede-6f3a4e6f7b3a
ms.date: 12/05/2018
ms.keywords: IXpsOMRemoteDictionaryResource interface [XPS Documents and Packaging],SetDictionary method, IXpsOMRemoteDictionaryResource.SetDictionary, IXpsOMRemoteDictionaryResource::SetDictionary, SetDictionary, SetDictionary method [XPS Documents and Packaging], SetDictionary method [XPS Documents and Packaging],IXpsOMRemoteDictionaryResource interface, xps.ixpsomremotedictionaryresource_setdictionary, xpsobjectmodel/IXpsOMRemoteDictionaryResource::SetDictionary
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
 - IXpsOMRemoteDictionaryResource::SetDictionary
 - xpsobjectmodel/IXpsOMRemoteDictionaryResource::SetDictionary
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
 - IXpsOMRemoteDictionaryResource.SetDictionary
---

# IXpsOMRemoteDictionaryResource::SetDictionary


## -description

Sets a   pointer to the <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdictionary">IXpsOMDictionary</a> interface of the remote dictionary that is to be associated with this resource.

## -parameters

### -param dictionary [in]

The <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdictionary">IXpsOMDictionary</a> interface of the dictionary that is to be associated with this resource.

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
<i>dictionary</i> does not point to a recognized interface implementation. Custom implementation of XPS Document API interfaces is not supported.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomremotedictionaryresource">IXpsOMRemoteDictionaryResource</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>