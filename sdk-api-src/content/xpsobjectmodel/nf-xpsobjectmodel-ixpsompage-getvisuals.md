---
UID: NF:xpsobjectmodel.IXpsOMPage.GetVisuals
title: IXpsOMPage::GetVisuals
author: windows-sdk-content
description: Gets a pointer to an IXpsOMVisualCollection interface that contains a collection of the page's visual objects.
old-location: xps\ixpsompage_getvisuals.htm
tech.root: printdocs
ms.assetid: 8181513f-2a5d-4b43-aa40-7f886a8af7f7
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: GetVisuals, GetVisuals method [XPS Documents and Packaging], GetVisuals method [XPS Documents and Packaging],IXpsOMPage interface, IXpsOMPage interface [XPS Documents and Packaging],GetVisuals method, IXpsOMPage.GetVisuals, IXpsOMPage::GetVisuals, xps.ixpsompage_getvisuals, xpsobjectmodel/IXpsOMPage::GetVisuals
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
 - IXpsOMPage.GetVisuals
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- xpsobjectmodel.h
: 
- IXpsOMPage.GetVisuals
: 
---

# IXpsOMPage::GetVisuals


## -description


Gets a pointer to an <a href="https://msdn.microsoft.com/f373b437-3973-40aa-9cac-a6b196a3e5d1">IXpsOMVisualCollection</a> interface that contains a collection  of the page's visual objects.


## -parameters




### -param visuals [out, retval]

A pointer to the <a href="https://msdn.microsoft.com/f373b437-3973-40aa-9cac-a6b196a3e5d1">IXpsOMVisualCollection</a>  interface that contains a collection  of the page's visual objects.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the table that follows. For information about  XPS document API return values that are not listed in this table, see <a href="https://msdn.microsoft.com/9e6db1e3-7151-4538-8607-b7185ebc0110">XPS Document Errors</a>.

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
<i>visuals</i> is <b>NULL</b>.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/741deebd-9dce-4cd9-883e-4586c10a4609">IXpsOMPage</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://msdn.microsoft.com/9e6db1e3-7151-4538-8607-b7185ebc0110">XPS Document Errors</a>
 

 

