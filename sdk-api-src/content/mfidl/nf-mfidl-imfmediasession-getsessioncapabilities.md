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

# IMFMediaSession::GetSessionCapabilities


## -description



Retrieves the capabilities of the Media Session, based on the current presentation.




## -parameters




### -param pdwCaps [out]

Receives a bitwise <b>OR</b> of zero or more of the following flags.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MFSESSIONCAP_PAUSE"></a><a id="mfsessioncap_pause"></a><dl>
<dt><b>MFSESSIONCAP_PAUSE</b></dt>
</dl>
</td>
<td width="60%">
The Media Session can be paused.

</td>
</tr>
<tr>
<td width="40%"><a id="MFSESSIONCAP_RATE_FORWARD"></a><a id="mfsessioncap_rate_forward"></a><dl>
<dt><b>MFSESSIONCAP_RATE_FORWARD</b></dt>
</dl>
</td>
<td width="60%">
The Media Session supports forward playback at rates faster than 1.0.

</td>
</tr>
<tr>
<td width="40%"><a id="MFSESSIONCAP_RATE_REVERSE"></a><a id="mfsessioncap_rate_reverse"></a><dl>
<dt><b>MFSESSIONCAP_RATE_REVERSE</b></dt>
</dl>
</td>
<td width="60%">
The Media Session supports reverse playback.

</td>
</tr>
<tr>
<td width="40%"><a id="MFSESSIONCAP_SEEK"></a><a id="mfsessioncap_seek"></a><dl>
<dt><b>MFSESSIONCAP_SEEK</b></dt>
</dl>
</td>
<td width="60%">
The Media Session can be seeked.

</td>
</tr>
<tr>
<td width="40%"><a id="MFSESSIONCAP_START"></a><a id="mfsessioncap_start"></a><dl>
<dt><b>MFSESSIONCAP_START</b></dt>
</dl>
</td>
<td width="60%">
The Media Session can be started.

</td>
</tr>
</table>
 


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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
NULL pointer argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_SHUTDOWN</b></dt>
</dl>
</td>
<td width="60%">
The Media Session has been shut down.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/feebf891-73fa-4fe6-94ca-3594986fc92d">IMFMediaSession</a>
 

 

