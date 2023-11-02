---
UID: NF:xpsobjectmodel.IXpsOMDashCollection.GetAt
title: IXpsOMDashCollection::GetAt (xpsobjectmodel.h)
description: Gets an XPS_DASH structure from a specified location in the collection.
helpviewer_keywords: ["GetAt","GetAt method [XPS Documents and Packaging]","GetAt method [XPS Documents and Packaging]","IXpsOMDashCollection interface","IXpsOMDashCollection interface [XPS Documents and Packaging]","GetAt method","IXpsOMDashCollection.GetAt","IXpsOMDashCollection::GetAt","xps.ixpsomdashcollection_getat","xpsobjectmodel/IXpsOMDashCollection::GetAt"]
old-location: xps\ixpsomdashcollection_getat.htm
tech.root: xps
ms.assetid: 70749e4c-1f67-41e8-9def-85d38493c099
ms.date: 12/05/2018
ms.keywords: GetAt, GetAt method [XPS Documents and Packaging], GetAt method [XPS Documents and Packaging],IXpsOMDashCollection interface, IXpsOMDashCollection interface [XPS Documents and Packaging],GetAt method, IXpsOMDashCollection.GetAt, IXpsOMDashCollection::GetAt, xps.ixpsomdashcollection_getat, xpsobjectmodel/IXpsOMDashCollection::GetAt
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
 - IXpsOMDashCollection::GetAt
 - xpsobjectmodel/IXpsOMDashCollection::GetAt
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
 - IXpsOMDashCollection.GetAt
---

# IXpsOMDashCollection::GetAt


## -description

Gets an <a href="/windows/win32/api/xpsobjectmodel/ns-xpsobjectmodel-xps_dash">XPS_DASH</a> structure from a specified location in the collection.

## -parameters

### -param index [in]

The zero-based index in the collection where an <a href="/windows/win32/api/xpsobjectmodel/ns-xpsobjectmodel-xps_dash">XPS_DASH</a> structure is to  be obtained.

### -param dash [out, retval]

The <a href="/windows/win32/api/xpsobjectmodel/ns-xpsobjectmodel-xps_dash">XPS_DASH</a> structure that is found at the location specified by <i>index</i>.

## -returns

If the method succeeds, it returns S_OK; otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

For more information about the collection methods, see  <a href="/previous-versions/windows/desktop/dd372931(v=vs.85)">Working with XPS OM Collection Interfaces</a>.

## -see-also

<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdashcollection">IXpsOMDashCollection</a>



<a href="/previous-versions/windows/desktop/dd372931(v=vs.85)">Working with XPS OM Collection Interfaces</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/windows/win32/api/xpsobjectmodel/ns-xpsobjectmodel-xps_dash">XPS_DASH</a>