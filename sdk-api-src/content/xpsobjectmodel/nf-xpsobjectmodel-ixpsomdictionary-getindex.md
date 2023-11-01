---
UID: NF:xpsobjectmodel.IXpsOMDictionary.GetIndex
title: IXpsOMDictionary::GetIndex (xpsobjectmodel.h)
description: Gets the index of an IXpsOMShareable interface from the dictionary.
helpviewer_keywords: ["GetIndex","GetIndex method [XPS Documents and Packaging]","GetIndex method [XPS Documents and Packaging]","IXpsOMDictionary interface","IXpsOMDictionary interface [XPS Documents and Packaging]","GetIndex method","IXpsOMDictionary.GetIndex","IXpsOMDictionary::GetIndex","xps.ixpsomdictionary_getindex","xpsobjectmodel/IXpsOMDictionary::GetIndex"]
old-location: xps\ixpsomdictionary_getindex.htm
tech.root: printdocs
ms.assetid: dd3d8ff2-8674-4669-b7c5-6f97c957cc64
ms.date: 12/05/2018
ms.keywords: GetIndex, GetIndex method [XPS Documents and Packaging], GetIndex method [XPS Documents and Packaging],IXpsOMDictionary interface, IXpsOMDictionary interface [XPS Documents and Packaging],GetIndex method, IXpsOMDictionary.GetIndex, IXpsOMDictionary::GetIndex, xps.ixpsomdictionary_getindex, xpsobjectmodel/IXpsOMDictionary::GetIndex
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
 - IXpsOMDictionary::GetIndex
 - xpsobjectmodel/IXpsOMDictionary::GetIndex
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
 - IXpsOMDictionary.GetIndex
---

# IXpsOMDictionary::GetIndex


## -description

Gets the index of an <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomshareable">IXpsOMShareable</a> interface from the dictionary.

## -parameters

### -param entry [in]

The <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomshareable">IXpsOMShareable</a> interface pointer to be found in the dictionary.

### -param index [out, retval]

The zero-based index of <i>entry</i> in the dictionary.

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
<dt><b>E_INVALIDARG
</b></dt>
</dl>
</td>
<td width="60%">
The object referenced by <i>entry</i> is not in the dictionary.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdictionary">IXpsOMDictionary</a>



<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomshareable">IXpsOMShareable</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>