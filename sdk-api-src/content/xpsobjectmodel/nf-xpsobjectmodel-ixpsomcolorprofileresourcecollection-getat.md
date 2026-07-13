---
UID: NF:xpsobjectmodel.IXpsOMColorProfileResourceCollection.GetAt
title: IXpsOMColorProfileResourceCollection::GetAt (xpsobjectmodel.h)
description: Gets an IXpsOMColorProfileResource interface pointer from a specified location in the collection.
helpviewer_keywords: ["GetAt","GetAt method [XPS Documents and Packaging]","GetAt method [XPS Documents and Packaging]","IXpsOMColorProfileResourceCollection interface","IXpsOMColorProfileResourceCollection interface [XPS Documents and Packaging]","GetAt method","IXpsOMColorProfileResourceCollection.GetAt","IXpsOMColorProfileResourceCollection::GetAt","xps.ixpsomcolorprofileresourcecollection_getat","xpsobjectmodel/IXpsOMColorProfileResourceCollection::GetAt"]
old-location: xps\ixpsomcolorprofileresourcecollection_getat.htm
tech.root: xps
ms.assetid: ecb8b3e7-182f-446a-bc12-28762da1f930
ms.date: 12/05/2018
ms.keywords: GetAt, GetAt method [XPS Documents and Packaging], GetAt method [XPS Documents and Packaging],IXpsOMColorProfileResourceCollection interface, IXpsOMColorProfileResourceCollection interface [XPS Documents and Packaging],GetAt method, IXpsOMColorProfileResourceCollection.GetAt, IXpsOMColorProfileResourceCollection::GetAt, xps.ixpsomcolorprofileresourcecollection_getat, xpsobjectmodel/IXpsOMColorProfileResourceCollection::GetAt
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
 - IXpsOMColorProfileResourceCollection::GetAt
 - xpsobjectmodel/IXpsOMColorProfileResourceCollection::GetAt
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
 - IXpsOMColorProfileResourceCollection.GetAt
---

# IXpsOMColorProfileResourceCollection::GetAt


## -description

Gets an <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcolorprofileresource">IXpsOMColorProfileResource</a> interface pointer from a specified location in the collection.

## -parameters

### -param index [in]

The zero-based index of the <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcolorprofileresource">IXpsOMColorProfileResource</a> interface pointer to be obtained.

### -param object [out, retval]

The <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcolorprofileresource">IXpsOMColorProfileResource</a> interface pointer at the location specified by <i>index</i>.

## -returns

If the method succeeds, it returns S_OK; otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

For more information about the collection methods, see  <a href="/previous-versions/windows/desktop/dd372931(v=vs.85)">Working with XPS OM Collection Interfaces</a>.

## -see-also

<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcolorprofileresource">IXpsOMColorProfileResource</a>



<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcolorprofileresourcecollection">IXpsOMColorProfileResourceCollection</a>



<a href="/previous-versions/windows/desktop/dd372931(v=vs.85)">Working with XPS OM Collection Interfaces</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>