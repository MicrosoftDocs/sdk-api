---
UID: NF:mfidl.IMFMediaSession.GetSessionCapabilities
title: IMFMediaSession::GetSessionCapabilities
author: windows-sdk-content
description: Retrieves the capabilities of the Media Session, based on the current presentation.
old-location: mf\imfmediasession_getsessioncapabilities.htm
old-project: medfound
ms.assetid: 3534cfb9-23ff-42a6-a3db-b5032d427cf2
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: 3534cfb9-23ff-42a6-a3db-b5032d427cf2, GetSessionCapabilities, GetSessionCapabilities method [Media Foundation], GetSessionCapabilities method [Media Foundation],IMFMediaSession interface, IMFMediaSession interface [Media Foundation],GetSessionCapabilities method, IMFMediaSession.GetSessionCapabilities, IMFMediaSession::GetSessionCapabilities, MFSESSIONCAP_PAUSE, MFSESSIONCAP_RATE_FORWARD, MFSESSIONCAP_RATE_REVERSE, MFSESSIONCAP_SEEK, MFSESSIONCAP_START, mf.imfmediasession_getsessioncapabilities, mfidl/IMFMediaSession::GetSessionCapabilities
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: MFSensorDeviceMode
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mfuuid.lib
-	mfuuid.dll
api_name:
-	IMFMediaSession.GetSessionCapabilities
product: Windows
targetos: Windows
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
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
 

 

