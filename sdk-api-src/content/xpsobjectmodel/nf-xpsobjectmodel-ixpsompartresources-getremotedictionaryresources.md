---
UID: NF:xpsobjectmodel.IXpsOMPartResources.GetRemoteDictionaryResources
title: IXpsOMPartResources::GetRemoteDictionaryResources (xpsobjectmodel.h)
description: Gets the IXpsOMRemoteDictionaryResourceCollection interface that contains the remote resource dictionaries that are used in the XPS document.
helpviewer_keywords: ["GetRemoteDictionaryResources","GetRemoteDictionaryResources method [XPS Documents and Packaging]","GetRemoteDictionaryResources method [XPS Documents and Packaging]","IXpsOMPartResources interface","IXpsOMPartResources interface [XPS Documents and Packaging]","GetRemoteDictionaryResources method","IXpsOMPartResources.GetRemoteDictionaryResources","IXpsOMPartResources::GetRemoteDictionaryResources","xps.ixpsompartresources_getremotedictionaryresources","xpsobjectmodel/IXpsOMPartResources::GetRemoteDictionaryResources"]
old-location: xps\ixpsompartresources_getremotedictionaryresources.htm
tech.root: xps
ms.assetid: cb12fe80-9e94-4797-adf5-a1986512bf57
ms.date: 12/05/2018
ms.keywords: GetRemoteDictionaryResources, GetRemoteDictionaryResources method [XPS Documents and Packaging], GetRemoteDictionaryResources method [XPS Documents and Packaging],IXpsOMPartResources interface, IXpsOMPartResources interface [XPS Documents and Packaging],GetRemoteDictionaryResources method, IXpsOMPartResources.GetRemoteDictionaryResources, IXpsOMPartResources::GetRemoteDictionaryResources, xps.ixpsompartresources_getremotedictionaryresources, xpsobjectmodel/IXpsOMPartResources::GetRemoteDictionaryResources
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
 - IXpsOMPartResources::GetRemoteDictionaryResources
 - xpsobjectmodel/IXpsOMPartResources::GetRemoteDictionaryResources
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
 - IXpsOMPartResources.GetRemoteDictionaryResources
---

# IXpsOMPartResources::GetRemoteDictionaryResources


## -description

Gets the  <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomremotedictionaryresourcecollection">IXpsOMRemoteDictionaryResourceCollection</a> interface that contains the remote resource dictionaries  that are used in the XPS document.

## -parameters

### -param dictionaryResources [out, retval]

A pointer to the <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomremotedictionaryresourcecollection">IXpsOMRemoteDictionaryResourceCollection</a> interface that  contains the remote resource dictionaries that are used in the XPS document.

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
<i>dictionaryResources</i> is <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

After loading and parsing the resource into the XPS OM, this method might return an error that applies to another resource. This occurs because all of the relationships are parsed when a resource is loaded.

## -see-also

<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompartresources">IXpsOMPartResources</a>



<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomremotedictionaryresourcecollection">IXpsOMRemoteDictionaryResourceCollection</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>