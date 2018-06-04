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

# IWMIStreamProps::GetProperty


## -description



The <b>GetProperty</b> method retrieves a named property from the <b>IStream</b>.




## -parameters




### -param pszName [in]

Pointer to a <b>null</b>-terminated string containing the name of the property to retrieve. You should use the global identifier to refer to properties so that any error will appear at compile time. The following table lists the available <b>IStream</b> properties.

<table>
<tr>
<th>
                  Property name
                </th>
<th>
                  Global identifier
                </th>
</tr>
<tr>
<td><b>ReloadIndexOnSeek</b></td>
<td>g_wszReloadIndexOnSeek</td>
</tr>
<tr>
<td><b>StreamNumIndexObjects</b></td>
<td>g_wszStreamNumIndexObjects</td>
</tr>
<tr>
<td><b>FailSeekOnError</b></td>
<td>g_wszFailSeekOnError</td>
</tr>
<tr>
<td><b>PermitSeeksBeyondEndOfStream</b></td>
<td>g_wszPermitSeeksBeyondEndOfStream</td>
</tr>
<tr>
<td><b>UsePacketAtSeekPoint</b></td>
<td>g_wszUsePacketAtSeekPoint</td>
</tr>
<tr>
<td><b>SourceBufferTime</b></td>
<td>g_wszSourceBufferTime</td>
</tr>
<tr>
<td><b>SourceMaxBytesAtOnce</b></td>
<td>g_wszSourceMaxBytesAtOnce</td>
</tr>
</table>
 


### -param pType [out]

Pointer to a variable that will receive one member of the <a href="https://msdn.microsoft.com/2a2756f9-2d76-48c9-bbea-35ee33a39918">WMT_ATTR_DATATYPE</a> enumeration type. This value indicates the type of data in the buffer at <i>pValue</i>.


### -param pValue [out]

Pointer to a byte buffer that will receive the property value. The type of data returned to the buffer is indicated by the value pointed to by <i>pType</i>.


### -param pdwSize [in, out]

Pointer to a <b>DWORD</b> containing the size of the buffer at <i>pValue</i>. On return, this value will be set to the correct size of the property value.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

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
<i>pType</i>, <i>pValue</i>, or <i>pdwSize</i> is <b>NULL</b>.

OR

The buffer is not big enough to hold the requested value.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
<i>pszName</i> specifies an invalid property name.

</td>
</tr>
</table>
 




## -remarks



You should make two calls to <b>GetProperty</b> for each property you want to retrieve. On the first call, pass <b>NULL</b> as <i>pValue</i>. On return, the value pointed to by <i>pdwSize</i> will be set to the buffer size required to hold the property value. Then you can allocate the required amount of memory for the buffer and pass a pointer to it as <i>pValue</i> on the second call.




## -see-also




<a href="https://msdn.microsoft.com/336e11ce-6212-4d08-8c50-76b2128ddc35">IWMIStreamProps Interface</a>
 

 

