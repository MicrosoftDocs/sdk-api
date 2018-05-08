---
UID: NF:xpsobjectmodel.IXpsOMPath.SetStrokeDashCap
title: IXpsOMPath::SetStrokeDashCap
author: windows-driver-content
description: Sets the style of the stroke's dash cap.
old-location: xps\ixpsompath_setstrokedashcap.htm
old-project: printdocs
ms.assetid: 949f366b-1161-4db8-b9b9-d95b422b8931
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: IXpsOMPath interface [XPS Documents and Packaging],SetStrokeDashCap method, IXpsOMPath.SetStrokeDashCap, IXpsOMPath::SetStrokeDashCap, SetStrokeDashCap, SetStrokeDashCap method [XPS Documents and Packaging], SetStrokeDashCap method [XPS Documents and Packaging],IXpsOMPath interface, xps.ixpsompath_setstrokedashcap, xpsobjectmodel/IXpsOMPath::SetStrokeDashCap
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: xpsobjectmodel.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: XpsObjectModel.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: XPS_INTERLEAVING
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	xpsobjectmodel.h
api_name:
-	IXpsOMPath.SetStrokeDashCap
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IXpsOMPath::SetStrokeDashCap


## -description


Sets the style of the stroke's dash cap.


## -parameters




### -param strokeDashCap [in]

The <a href="https://msdn.microsoft.com/8c4d7314-71ad-4700-bc3e-f611e72c05df">XPS_DASH_CAP</a> value to be set.


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
<dt><b>E_INVALIDARG </b></dt>
</dl>
</td>
<td width="60%">
<i>strokeDashCap</i> was not a valid <a href="https://msdn.microsoft.com/8c4d7314-71ad-4700-bc3e-f611e72c05df">XPS_DASH_CAP</a> value.

</td>
</tr>
</table>
 




## -remarks



For more information about dash cap styles, see <a href="https://msdn.microsoft.com/8c4d7314-71ad-4700-bc3e-f611e72c05df">XPS_DASH_CAP</a>.




## -see-also




<a href="https://msdn.microsoft.com/93257a77-3fef-400e-bfe1-06e760ba4b93">IXpsOMPath</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://msdn.microsoft.com/9e6db1e3-7151-4538-8607-b7185ebc0110">XPS Document Errors</a>



<a href="https://msdn.microsoft.com/8c4d7314-71ad-4700-bc3e-f611e72c05df">XPS_DASH_CAP</a>
 

 

