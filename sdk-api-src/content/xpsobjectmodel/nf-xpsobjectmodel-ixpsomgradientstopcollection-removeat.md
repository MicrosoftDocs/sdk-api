---
UID: NF:xpsobjectmodel.IXpsOMGradientStopCollection.RemoveAt
title: IXpsOMGradientStopCollection::RemoveAt (xpsobjectmodel.h)
author: windows-sdk-content
description: Removes and releases an IXpsOMGradientStop interface pointer from a specified location in the collection.
old-location: xps\ixpsomgradientstopcollection_removeat.htm
tech.root: printdocs
ms.assetid: dbca41b1-5510-484d-80a1-c8d260cb5c39
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IXpsOMGradientStopCollection interface [XPS Documents and Packaging],RemoveAt method, IXpsOMGradientStopCollection.RemoveAt, IXpsOMGradientStopCollection::RemoveAt, RemoveAt, RemoveAt method [XPS Documents and Packaging], RemoveAt method [XPS Documents and Packaging],IXpsOMGradientStopCollection interface, xps.ixpsomgradientstopcollection_removeat, xpsobjectmodel/IXpsOMGradientStopCollection::RemoveAt
ms.topic: method
f1_keywords: ["xpsobjectmodel/IXpsOMGradientStopCollection.RemoveAt"]
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
 - IXpsOMGradientStopCollection.RemoveAt
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IXpsOMGradientStopCollection::RemoveAt


## -description


Removes and releases an <a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgradientstop">IXpsOMGradientStop</a> interface pointer from a specified location in the collection.


## -parameters




### -param index [in]

The zero-based index in the collection from which  an <a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgradientstop">IXpsOMGradientStop</a> interface pointer is to be removed and released.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the table that follows. For information about  XPS document API return values that are not listed in this table, see <a href="https://docs.microsoft.com/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>.

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The gradient stop collection has only two stops.   A gradient stop collection must have at least two gradient stops, and removing the specified gradient stop would leave fewer than two gradient stops in the collection.

</td>
</tr>
</table>
 




## -remarks



This method releases the <a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgradientstop">IXpsOMGradientStop</a> interface  referenced by the pointer at  the location specified by <i>index</i>. After releasing the interface, this method compacts the collection by   reducing by 1 the index of each pointer subsequent to <i>index</i>.

For more information about the collection methods, see  <a href="https://docs.microsoft.com/previous-versions/windows/desktop/dd372931(v=vs.85)">Working with XPS OM Collection Interfaces</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgradientstop">IXpsOMGradientStop</a>



<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgradientstopcollection">IXpsOMGradientStopCollection</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/dd372931(v=vs.85)">Working with XPS OM Collection Interfaces</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>
 

 

