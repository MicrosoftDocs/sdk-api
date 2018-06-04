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

# ITextDocument2::GetClientRect


## -description


Retrieves the client rectangle of the rich edit control.


## -parameters




### -param Type [in]

Type: <b>long</b>

The client rectangle retrieval options. It can be a combination of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="tomClientCoord"></a><a id="tomclientcoord"></a><a id="TOMCLIENTCOORD"></a><dl>
<dt><b>tomClientCoord</b></dt>
</dl>
</td>
<td width="60%">
Retrieve the rectangle in client coordinates. If this value isn't specified, the function retrieves screen coordinates.

</td>
</tr>
<tr>
<td width="40%"><a id="tomIncludeInset"></a><a id="tomincludeinset"></a><a id="TOMINCLUDEINSET"></a><dl>
<dt><b>tomIncludeInset</b></dt>
</dl>
</td>
<td width="60%">
Add left and top insets to the left and top coordinates of the client rectangle, and subtract right and bottom insets from the right and bottom coordinates. 

</td>
</tr>
<tr>
<td width="40%"><a id="tomTransform"></a><a id="tomtransform"></a><a id="TOMTRANSFORM"></a><dl>
<dt><b>tomTransform</b></dt>
</dl>
</td>
<td width="60%">
Use a world transform (XFORM) provided by the host application to transform the retrieved rectangle  coordinates.

</td>
</tr>
</table>
 


### -param pLeft [out]

Type: <b>long*</b>

The x-coordinate of the upper-left corner of the rectangle.


### -param pTop [out]

Type: <b>long*</b>

The y-coordinate of the upper-left corner of the rectangle.


### -param pRight [out]

Type: <b>long*</b>

The x-coordinate of the lower-right corner of the rectangle.


### -param pBottom [out]

Type: <b>long*</b>

The y-coordinate of the lower-right corner of the rectangle.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/0b0a54d7-7606-41f6-b8be-6367d9180ef4">ITextDocument2</a>
 

 

