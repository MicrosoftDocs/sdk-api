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

# ITextHost::TxGetBackStyle


## -description


Requests the background style of the text host.


## -parameters




### -param pstyle

Type: <b>TXTBACKSTYLE*</b>

A variable that the text host sets to indicate the background style. The style is one of the following values from the 
					<b>TXTBACKSTYLE</b> enumeration.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TXTBACK_TRANSPARENT"></a><a id="txtback_transparent"></a><dl>
<dt><b>TXTBACK_TRANSPARENT</b></dt>
</dl>
</td>
<td width="60%">
Background shows through. 

</td>
</tr>
<tr>
<td width="40%"><a id="TXTBACK_OPAQUE"></a><a id="txtback_opaque"></a><dl>
<dt><b>TXTBACK_OPAQUE</b></dt>
</dl>
</td>
<td width="60%">
Background does not show through. 

</td>
</tr>
</table>
 


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

The return value is <b>S_OK</b>.




## -see-also




<a href="https://msdn.microsoft.com/28d86b94-2d36-4749-8954-3857bf6dbdac">ITextHost</a>



<a href="https://msdn.microsoft.com/71ecd220-ab1a-4caa-b1b9-0951e943692e">Windowless Rich Edit Controls Overview</a>
 

 

