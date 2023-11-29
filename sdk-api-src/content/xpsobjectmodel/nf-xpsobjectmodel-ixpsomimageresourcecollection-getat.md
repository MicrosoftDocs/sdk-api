---
UID: NF:xpsobjectmodel.IXpsOMImageResourceCollection.GetAt
title: IXpsOMImageResourceCollection::GetAt (xpsobjectmodel.h)
description: Gets an IXpsOMImageResource interface pointer from a specified location in the collection.
helpviewer_keywords: ["GetAt","GetAt method [XPS Documents and Packaging]","GetAt method [XPS Documents and Packaging]","IXpsOMImageResourceCollection interface","IXpsOMImageResourceCollection interface [XPS Documents and Packaging]","GetAt method","IXpsOMImageResourceCollection.GetAt","IXpsOMImageResourceCollection::GetAt","xps.ixpsomimageresourcecollection_getat","xpsobjectmodel/IXpsOMImageResourceCollection::GetAt"]
old-location: xps\ixpsomimageresourcecollection_getat.htm
tech.root: xps
ms.assetid: 31d4989d-72bd-4065-a0d7-c1ba5bea8391
ms.date: 12/05/2018
ms.keywords: GetAt, GetAt method [XPS Documents and Packaging], GetAt method [XPS Documents and Packaging],IXpsOMImageResourceCollection interface, IXpsOMImageResourceCollection interface [XPS Documents and Packaging],GetAt method, IXpsOMImageResourceCollection.GetAt, IXpsOMImageResourceCollection::GetAt, xps.ixpsomimageresourcecollection_getat, xpsobjectmodel/IXpsOMImageResourceCollection::GetAt
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
 - IXpsOMImageResourceCollection::GetAt
 - xpsobjectmodel/IXpsOMImageResourceCollection::GetAt
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
 - IXpsOMImageResourceCollection.GetAt
---

# IXpsOMImageResourceCollection::GetAt


## -description

Gets an <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomimageresource">IXpsOMImageResource</a> interface pointer from a specified location in the collection.

## -parameters

### -param index [in]

The zero-based index of the <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomimageresource">IXpsOMImageResource</a> interface pointer to be obtained.

### -param object [out, retval]

The <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomimageresource">IXpsOMImageResource</a> interface pointer at the location specified by <i>index</i>.

## -returns

If the method succeeds, it returns S_OK; otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

For more information about the collection methods, see  <a href="/previous-versions/windows/desktop/dd372931(v=vs.85)">Working with XPS OM Collection Interfaces</a>.

## -see-also

<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomimageresource">IXpsOMImageResource</a>



<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomimageresourcecollection">IXpsOMImageResourceCollection</a>



<a href="/previous-versions/windows/desktop/dd372931(v=vs.85)">Working with XPS OM Collection Interfaces</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>