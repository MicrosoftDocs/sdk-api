---
UID: NF:xpsobjectmodel.IXpsOMPath.GetSnapsToPixels
title: IXpsOMPath::GetSnapsToPixels
author: windows-sdk-content
description: Gets a Boolean value that indicates whether the path is to be snapped to device pixels when the path is rendered.
old-location: xps\ixpsompath_getsnapstopixels.htm
tech.root: printdocs
ms.assetid: c0a4a8b5-f7cf-4cbe-9221-41cde4f63557
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: FALSE, GetSnapsToPixels, GetSnapsToPixels method [XPS Documents and Packaging], GetSnapsToPixels method [XPS Documents and Packaging],IXpsOMPath interface, IXpsOMPath interface [XPS Documents and Packaging],GetSnapsToPixels method, IXpsOMPath.GetSnapsToPixels, IXpsOMPath::GetSnapsToPixels, TRUE, xps.ixpsompath_getsnapstopixels, xpsobjectmodel/IXpsOMPath::GetSnapsToPixels
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
 - IXpsOMPath.GetSnapsToPixels
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
- IXpsOMPath.GetSnapsToPixels
: 
---

# IXpsOMPath::GetSnapsToPixels


## -description


Gets a Boolean value that indicates whether the path is to  be snapped to device pixels when the path is rendered.


## -parameters




### -param snapsToPixels [out, retval]

A Boolean value that indicates whether the path is to be snapped to device pixels when the path is rendered. The following table describes the values possible  for this parameter.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TRUE"></a><a id="true"></a><dl>
<dt><b><b>TRUE</b></b></dt>
</dl>
</td>
<td width="60%">
The path is to be snapped to device pixels.

</td>
</tr>
<tr>
<td width="40%"><a id="FALSE"></a><a id="false"></a><dl>
<dt><b><b>FALSE</b></b></dt>
</dl>
</td>
<td width="60%">
The path is not to be snapped to device pixels.

</td>
</tr>
</table>
 


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
<i>snapsToPixels</i> is <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



The value returned by <b>GetSnapsToPixels</b> corresponds to the <b>SnapsToDevicePixels</b> element in the document markup.




## -see-also




<a href="https://msdn.microsoft.com/93257a77-3fef-400e-bfe1-06e760ba4b93">IXpsOMPath</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://msdn.microsoft.com/9e6db1e3-7151-4538-8607-b7185ebc0110">XPS Document Errors</a>
 

 

