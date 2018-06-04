---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IXpsOMCanvas::SetUseAliasedEdgeMode


## -description


Sets the value that determines whether the edges of objects in this canvas will be rendered using the aliased edge mode.


## -parameters




### -param useAliasedEdgeMode [in]

The Boolean value that determines whether  the edges of child objects in this canvas will be rendered using the aliased edge mode.

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
The edges of objects in the canvas are to be rendered without anti-aliasing using the aliased edge mode. This includes any objects that have this value set to <b>FALSE</b>.

In the document markup, this  corresponds  to the <b>RenderOptions.EdgeMode</b> attribute  having the value of <b>Aliased</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="FALSE"></a><a id="false"></a><dl>
<dt><b><b>FALSE</b></b></dt>
</dl>
</td>
<td width="60%">
The edges of objects in the canvas are to be rendered in the default manner.

In the document markup, this corresponds  to the <b>RenderOptions.EdgeMode</b> attribute being absent.

</td>
</tr>
</table>
 


## -returns



If the method succeeds, it returns S_OK; otherwise, it returns an <b>HRESULT</b> error code.




## -remarks



This property corresponds to the <b>RenderOptions.EdgeMode</b> attribute of the <b>Canvas</b> element in the document markup.




## -see-also




<a href="https://msdn.microsoft.com/3cb0e1b3-88a8-4724-a3c5-0df416294e62">IXpsOMCanvas</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>
 

 

