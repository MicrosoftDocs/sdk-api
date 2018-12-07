---
UID: NF:xpsobjectmodel.IXpsOMPath.SetSnapsToPixels
title: IXpsOMPath::SetSnapsToPixels
author: windows-sdk-content
description: Sets a Boolean value that indicates whether the path will be snapped to device pixels when that path is being rendered.
old-location: xps\ixpsompath_setsnapstopixels.htm
tech.root: printdocs
ms.assetid: 6b063829-3941-42be-bbe2-49b5a71b695a
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: FALSE, IXpsOMPath interface [XPS Documents and Packaging],SetSnapsToPixels method, IXpsOMPath.SetSnapsToPixels, IXpsOMPath::SetSnapsToPixels, SetSnapsToPixels, SetSnapsToPixels method [XPS Documents and Packaging], SetSnapsToPixels method [XPS Documents and Packaging],IXpsOMPath interface, TRUE, xps.ixpsompath_setsnapstopixels, xpsobjectmodel/IXpsOMPath::SetSnapsToPixels
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
 - IXpsOMPath.SetSnapsToPixels
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IXpsOMPath::SetSnapsToPixels


## -description


Sets a Boolean value that indicates whether the path will be snapped to device pixels when that path is being rendered.


## -parameters




### -param snapsToPixels [in]

A Boolean value that indicates whether to snap the path to the device pixels when that path is being rendered. The following table describes the values possible for this parameter.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TRUE"></a><a id="true"></a><dl>
<dt><b>TRUE</b></dt>
</dl>
</td>
<td width="60%">
Snap the path to the device pixels.

</td>
</tr>
<tr>
<td width="40%"><a id="FALSE"></a><a id="false"></a><dl>
<dt><b>FALSE</b></dt>
</dl>
</td>
<td width="60%">
Do not snap the path to the device pixels.

</td>
</tr>
</table>
 


## -returns



If the method succeeds, it returns S_OK; otherwise, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/93257a77-3fef-400e-bfe1-06e760ba4b93">IXpsOMPath</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>
 

 

