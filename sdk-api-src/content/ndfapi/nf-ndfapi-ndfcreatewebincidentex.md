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

# NdfCreateWebIncidentEx function


## -description


The <b>NdfCreateWebIncidentEx</b> function diagnoses web connectivity problems concerning a specific URL.  This function allows for more control over the underlying diagnosis than the <a href="https://msdn.microsoft.com/28ca2949-6867-4c9a-aebc-bf2a57627c04">NdfCreateWebIncident</a> function.


## -parameters




### -param url [in]

Type: <b>LPCWSTR</b>

The URL with which there is a connectivity issue.


### -param useWinHTTP [in]

Type: <b>BOOL</b>

<b>TRUE</b> if diagnosis will be performed using the WinHTTP APIs;  <b>FALSE</b> if the WinInet APIs will be used. 


### -param moduleName [in]

Type: <b>LPWSTR</b>

The module name to use when checking against application-specific filtering rules (for example, "C:\Program Files\Internet Explorer\iexplorer.exe").  If <b>NULL</b>, the value is autodetected during the diagnosis.


### -param handle [out]

Type: <b>NDFHANDLE*</b>

Handle to the Network Diagnostics Framework incident.


## -returns



Type: <b>HRESULT</b>

Possible return values include, but are not limited to, the following.

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
The operation succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ABORT</b></dt>
</dl>
</td>
<td width="60%">
The underlying diagnosis or repair operation has been canceled.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
There is not enough memory available to complete this operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NDF_E_BAD_PARAM</b></dt>
</dl>
</td>
<td width="60%">
One or more parameters are invalid.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/28ca2949-6867-4c9a-aebc-bf2a57627c04">NdfCreateWebIncident</a>
 

 

