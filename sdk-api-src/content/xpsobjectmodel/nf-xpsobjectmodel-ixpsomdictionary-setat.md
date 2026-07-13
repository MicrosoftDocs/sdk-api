---
UID: NF:xpsobjectmodel.IXpsOMDictionary.SetAt
title: IXpsOMDictionary::SetAt (xpsobjectmodel.h)
description: Replaces the entry at a specified location in the dictionary.
helpviewer_keywords: ["IXpsOMDictionary interface [XPS Documents and Packaging]","SetAt method","IXpsOMDictionary.SetAt","IXpsOMDictionary::SetAt","SetAt","SetAt method [XPS Documents and Packaging]","SetAt method [XPS Documents and Packaging]","IXpsOMDictionary interface","xps.ixpsomdictionary_setat","xpsobjectmodel/IXpsOMDictionary::SetAt"]
old-location: xps\ixpsomdictionary_setat.htm
tech.root: xps
ms.assetid: 834504f6-1c79-4a88-8c7b-69efd8b798c4
ms.date: 12/05/2018
ms.keywords: IXpsOMDictionary interface [XPS Documents and Packaging],SetAt method, IXpsOMDictionary.SetAt, IXpsOMDictionary::SetAt, SetAt, SetAt method [XPS Documents and Packaging], SetAt method [XPS Documents and Packaging],IXpsOMDictionary interface, xps.ixpsomdictionary_setat, xpsobjectmodel/IXpsOMDictionary::SetAt
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
 - IXpsOMDictionary::SetAt
 - xpsobjectmodel/IXpsOMDictionary::SetAt
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
 - IXpsOMDictionary.SetAt
---

# IXpsOMDictionary::SetAt


## -description

Replaces the entry at a specified location in the dictionary.

## -parameters

### -param index [in]

The zero-based index in the dictionary in which an  entry is to be replaced.

### -param key [in]

The key to be used for the new entry.

The string referenced by <i>key</i> must be unique in the dictionary.

### -param entry [in]

The <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomshareable">IXpsOMShareable</a> interface pointer that will replace current contents at the location specified by <i>index</i>.

A dictionary cannot contain duplicate interface pointers. This parameter must contain an interface pointer that is not already in the dictionary.

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
<i>entry</i> does not point to a recognized interface implementation. Custom implementation of XPS Document API interfaces is not supported.

</td>
</tr>
</table>

## -remarks

At the location specified by <i>index</i>, this method releases the <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomshareable">IXpsOMShareable</a> interface referenced by the existing pointer, then replaces it with the interface pointer that is passed in <i>entry</i> and assigns it the key passed in <i>key</i>.

The interface pointers stored in a dictionary will usually point to interfaces, such as <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsombrush">IXpsOMBrush</a>                 and <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisual">IXpsOMVisual</a>, that are derived from the <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomshareable">IXpsOMShareable</a> interface. To determine the interface type, call the <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomshareable-gettype">GetType</a> method.

The figure that follows illustrates how the dictionary is changed by the <b>SetAt</b> method.

<img alt="A figure that shows how RemoveAt removes an entry from the dictionary" src="./images/dictionary_setat.png"/>

## -see-also

<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdictionary">IXpsOMDictionary</a>



<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomshareable">IXpsOMShareable</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>