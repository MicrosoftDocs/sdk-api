---
UID: NF:xpsobjectmodel.IXpsOMRemoteDictionaryResourceCollection.GetAt
title: IXpsOMRemoteDictionaryResourceCollection::GetAt (xpsobjectmodel.h)
description: Gets an IXpsOMRemoteDictionaryResource interface pointer from a specified location in the collection.
helpviewer_keywords: ["GetAt","GetAt method [XPS Documents and Packaging]","GetAt method [XPS Documents and Packaging]","IXpsOMRemoteDictionaryResourceCollection interface","IXpsOMRemoteDictionaryResourceCollection interface [XPS Documents and Packaging]","GetAt method","IXpsOMRemoteDictionaryResourceCollection.GetAt","IXpsOMRemoteDictionaryResourceCollection::GetAt","xps.ixpsomremotedictionaryresourcecollection_getat","xpsobjectmodel/IXpsOMRemoteDictionaryResourceCollection::GetAt"]
old-location: xps\ixpsomremotedictionaryresourcecollection_getat.htm
tech.root: printdocs
ms.assetid: a8130a0b-ac58-479d-b72c-2136c7d29c7f
ms.date: 12/05/2018
ms.keywords: GetAt, GetAt method [XPS Documents and Packaging], GetAt method [XPS Documents and Packaging],IXpsOMRemoteDictionaryResourceCollection interface, IXpsOMRemoteDictionaryResourceCollection interface [XPS Documents and Packaging],GetAt method, IXpsOMRemoteDictionaryResourceCollection.GetAt, IXpsOMRemoteDictionaryResourceCollection::GetAt, xps.ixpsomremotedictionaryresourcecollection_getat, xpsobjectmodel/IXpsOMRemoteDictionaryResourceCollection::GetAt
f1_keywords:
- xpsobjectmodel/IXpsOMRemoteDictionaryResourceCollection.GetAt
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- xpsobjectmodel.h
api_name:
- IXpsOMRemoteDictionaryResourceCollection.GetAt
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IXpsOMRemoteDictionaryResourceCollection::GetAt


## -description


Gets an <a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomremotedictionaryresource">IXpsOMRemoteDictionaryResource</a> interface pointer from a specified location in the collection.


## -parameters




### -param index [in]

The zero-based index of the <a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomremotedictionaryresource">IXpsOMRemoteDictionaryResource</a> interface pointer to be obtained.


### -param object [out, retval]

The <a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomremotedictionaryresource">IXpsOMRemoteDictionaryResource</a> interface pointer at the location specified by <i>index</i>.


## -returns



If the method succeeds, it returns S_OK; otherwise, it returns an <b>HRESULT</b> error code.




## -remarks



For more information about the collection methods, see  <a href="https://docs.microsoft.com/previous-versions/windows/desktop/dd372931(v=vs.85)">Working with XPS OM Collection Interfaces</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomremotedictionaryresource">IXpsOMRemoteDictionaryResource</a>



<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomremotedictionaryresourcecollection">IXpsOMRemoteDictionaryResourceCollection</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/dd372931(v=vs.85)">Working with XPS OM Collection Interfaces</a>



<a href="https://www.microsoft.com/download/details.aspx?id=11816">XML Paper Specification</a>
 

 

