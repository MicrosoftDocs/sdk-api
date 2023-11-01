---
UID: NF:xpsobjectmodel.IXpsOMGradientStopCollection.GetAt
title: IXpsOMGradientStopCollection::GetAt (xpsobjectmodel.h)
description: Gets an IXpsOMGradientStop interface pointer from a specified location in the collection.
helpviewer_keywords: ["GetAt","GetAt method [XPS Documents and Packaging]","GetAt method [XPS Documents and Packaging]","IXpsOMGradientStopCollection interface","IXpsOMGradientStopCollection interface [XPS Documents and Packaging]","GetAt method","IXpsOMGradientStopCollection.GetAt","IXpsOMGradientStopCollection::GetAt","xps.ixpsomgradientstopcollection_getat","xpsobjectmodel/IXpsOMGradientStopCollection::GetAt"]
old-location: xps\ixpsomgradientstopcollection_getat.htm
tech.root: xps
ms.assetid: 5e75d595-0124-4239-b53e-f1b8101d2dcf
ms.date: 12/05/2018
ms.keywords: GetAt, GetAt method [XPS Documents and Packaging], GetAt method [XPS Documents and Packaging],IXpsOMGradientStopCollection interface, IXpsOMGradientStopCollection interface [XPS Documents and Packaging],GetAt method, IXpsOMGradientStopCollection.GetAt, IXpsOMGradientStopCollection::GetAt, xps.ixpsomgradientstopcollection_getat, xpsobjectmodel/IXpsOMGradientStopCollection::GetAt
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
 - IXpsOMGradientStopCollection::GetAt
 - xpsobjectmodel/IXpsOMGradientStopCollection::GetAt
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
 - IXpsOMGradientStopCollection.GetAt
---

# IXpsOMGradientStopCollection::GetAt


## -description

Gets an <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgradientstop">IXpsOMGradientStop</a> interface pointer from a specified location in the collection.

## -parameters

### -param index [in]

The zero-based index of the <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgradientstop">IXpsOMGradientStop</a> interface pointer to be obtained.

### -param stop [out, retval]

The <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgradientstop">IXpsOMGradientStop</a> interface pointer at the location specified by <i>index</i>.

## -returns

If the method succeeds, it returns S_OK; otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

For more information about the collection methods, see  <a href="/previous-versions/windows/desktop/dd372931(v=vs.85)">Working with XPS OM Collection Interfaces</a>.

## -see-also

<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgradientstop">IXpsOMGradientStop</a>



<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgradientstopcollection">IXpsOMGradientStopCollection</a>



<a href="/previous-versions/windows/desktop/dd372931(v=vs.85)">Working with XPS OM Collection Interfaces</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>