---
UID: NF:xpsobjectmodel.IXpsOMPageReference.GetAdvisoryPageDimensions
title: IXpsOMPageReference::GetAdvisoryPageDimensions
author: windows-sdk-content
description: Gets the suggested dimensions of the page.
old-location: xps\ixpsompagereference_getadvisorypagedimensions.htm
tech.root: printdocs
ms.assetid: 1e25d910-5ca5-4e92-8b77-479c48a0089a
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: GetAdvisoryPageDimensions, GetAdvisoryPageDimensions method [XPS Documents and Packaging], GetAdvisoryPageDimensions method [XPS Documents and Packaging],IXpsOMPageReference interface, IXpsOMPageReference interface [XPS Documents and Packaging],GetAdvisoryPageDimensions method, IXpsOMPageReference.GetAdvisoryPageDimensions, IXpsOMPageReference::GetAdvisoryPageDimensions, xps.ixpsompagereference_getadvisorypagedimensions, xpsobjectmodel/IXpsOMPageReference::GetAdvisoryPageDimensions
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
 - IXpsOMPageReference.GetAdvisoryPageDimensions
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IXpsOMPageReference::GetAdvisoryPageDimensions


## -description


Gets the suggested dimensions of the page.


## -parameters




### -param pageDimensions [out, retval]

The suggested dimensions of the page.

Size is described in XPS units. There are 96 XPS units per inch.  For example, the dimensions of an 8.5" by 11.0" page are 816 by 1,056 XPS units.


## -returns



If the method succeeds, it returns S_OK; otherwise, it returns an <b>HRESULT</b> error code.

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
<i>pageDimensions</i> is <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



<div class="alert"><b>Note</b>   If a dimension value has not been set, a value of –1.0 is returned for that dimension.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/cdebab24-f918-4235-b4d5-5ee1007ade87">IXpsOMPageReference</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://msdn.microsoft.com/2f6eb553-892b-455b-97a5-280f257b5702">XPS_SIZE</a>
 

 

