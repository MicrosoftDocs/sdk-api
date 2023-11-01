---
UID: NF:xpsobjectmodel.IXpsOMNameCollection.GetAt
title: IXpsOMNameCollection::GetAt (xpsobjectmodel.h)
description: Gets the name string that is stored at a specified location in the collection.
helpviewer_keywords: ["GetAt","GetAt method [XPS Documents and Packaging]","GetAt method [XPS Documents and Packaging]","IXpsOMNameCollection interface","IXpsOMNameCollection interface [XPS Documents and Packaging]","GetAt method","IXpsOMNameCollection.GetAt","IXpsOMNameCollection::GetAt","xps.ixpsomnamecollection_getat","xpsobjectmodel/IXpsOMNameCollection::GetAt"]
old-location: xps\ixpsomnamecollection_getat.htm
tech.root: xps
ms.assetid: 729e44fa-2080-4ae8-84d6-873329f90e4e
ms.date: 12/05/2018
ms.keywords: GetAt, GetAt method [XPS Documents and Packaging], GetAt method [XPS Documents and Packaging],IXpsOMNameCollection interface, IXpsOMNameCollection interface [XPS Documents and Packaging],GetAt method, IXpsOMNameCollection.GetAt, IXpsOMNameCollection::GetAt, xps.ixpsomnamecollection_getat, xpsobjectmodel/IXpsOMNameCollection::GetAt
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
 - IXpsOMNameCollection::GetAt
 - xpsobjectmodel/IXpsOMNameCollection::GetAt
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
 - IXpsOMNameCollection.GetAt
---

# IXpsOMNameCollection::GetAt


## -description

Gets the name string that is stored at a specified location in the collection.

## -parameters

### -param index [in]

The zero-based index of the collection that contains the name string to be obtained.

### -param name [out, retval]

The name string at the location specified by <i>index</i>.

## -returns

If the method succeeds, it returns S_OK; otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

For more information about the collection methods, see  <a href="/previous-versions/windows/desktop/dd372931(v=vs.85)">Working with XPS OM Collection Interfaces</a>.

This method allocates the memory used by the string that is returned in <i>name</i>.  If <i>name</i> is not <b>NULL</b>, use the <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a> function  to free the memory.

## -see-also

<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomnamecollection">IXpsOMNameCollection</a>



<a href="/previous-versions/windows/desktop/dd372931(v=vs.85)">Working with XPS OM Collection Interfaces</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>