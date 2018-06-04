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

# IMediaParamInfo::GetParamText


## -description



The <code>GetParamText</code> method retrieves a series of text strings that describe the parameter.




## -parameters




### -param dwParamIndex [in]

Zero-based index of the parameter.


### -param ppwchText [out]

Address of a variable that receives a pointer to a series of Unicode™ strings.


## -returns



Returns an <b>HRESULT</b> value. Possible values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Index out of range.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<b>NULL</b> pointer argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
</table>
 




## -remarks



If the method succeeds, *<i>ppwchText</i> points to a string with the following format:

<code>Name\0Unit\0Enum1\0Enum2\0...EnumN\0\0</code>

where

<ul>
<li><i>Name</i> is the name of the parameter.</li>
<li><i>Unit</i> is the name of the units; for example, milliseconds.</li>
<li><i>Enum1</i> through <i></i></li>
<li><i>EnumN</i> are descriptive names for the parameter's enumerated values. (Applies only to parameters of type MPT_ENUM.)</li>
</ul>
The application can display these values within its user interface. They are not guaranteed to follow a consistent naming scheme. If the user's computer is using an international code page, the method might return a localized string corresponding to that code page.

The object uses the <b>CoTaskMemAlloc</b> function to allocate memory for the string. After you call this method, call <b>CoTaskMemFree</b> to free the buffer.




## -see-also




<a href="https://msdn.microsoft.com/80c7da71-7898-4bda-a181-09ad8906532a">IMediaParamInfo Interface</a>
 

 

