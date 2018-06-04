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

# IXpsOMGeometry::SetFillRule


## -description


Sets the  <a href="https://msdn.microsoft.com/353a4dc3-0c4d-46df-ae31-cc94c4116ca3">XPS_FILL_RULE</a> value that describes the fill rule to be used.


## -parameters




### -param fillRule [in]

The <a href="https://msdn.microsoft.com/353a4dc3-0c4d-46df-ae31-cc94c4116ca3">XPS_FILL_RULE</a> value that describes the fill rule to be used.


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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>fillRule</i> is not a valid <a href="https://msdn.microsoft.com/353a4dc3-0c4d-46df-ae31-cc94c4116ca3">XPS_FILL_RULE</a> value.

</td>
</tr>
</table>
 




## -remarks



For more information about how the file rule determines whether a point is inside the fill region, see <a href="https://msdn.microsoft.com/353a4dc3-0c4d-46df-ae31-cc94c4116ca3">XPS_FILL_RULE</a>. 

In the document markup, this value corresponds to the <b>FillRule</b> attribute of the <b>PathGeometry</b> element.




## -see-also




<a href="https://msdn.microsoft.com/d3f74c1e-49ef-40ee-a2f4-b6d198b57624">IXpsOMGeometry</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://msdn.microsoft.com/9e6db1e3-7151-4538-8607-b7185ebc0110">XPS Document Errors</a>



<a href="https://msdn.microsoft.com/353a4dc3-0c4d-46df-ae31-cc94c4116ca3">XPS_FILL_RULE</a>
 

 

