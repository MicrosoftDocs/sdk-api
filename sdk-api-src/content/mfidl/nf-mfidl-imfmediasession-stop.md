---
UID: NF:mfidl.IMFMediaSession.Stop
title: IMFMediaSession::Stop method
author: windows-driver-content
description: Stops the Media Session.
old-location: mf\imfmediasession_stop.htm
old-project: medfound
ms.assetid: 9cc769cc-24ef-4790-a10e-4aec8fb4fc1f
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: 9cc769cc-24ef-4790-a10e-4aec8fb4fc1f, IMFMediaSession, IMFMediaSession interface [Media Foundation], Stop method, IMFMediaSession::Stop, Stop method [Media Foundation], Stop method [Media Foundation], IMFMediaSession interface, Stop,IMFMediaSession.Stop, mf.imfmediasession_stop, mfidl/IMFMediaSession::Stop
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: MF_URL_TRUST_STATUS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mfuuid.lib
-	mfuuid.dll
api_name:
-	IMFMediaSession.Stop
product: Windows
targetos: Windows
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFMediaSession::Stop method


## -description



Stops the Media Session.




## -parameters






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
<dt><b>MF_E_INVALIDREQUEST</b></dt>
</dl>
</td>
<td width="60%">
The operation cannot be performed in the Media Session's current state.

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
 




## -remarks



This method is asynchronous. When the operation completes, the Media Session sends an <a href="https://msdn.microsoft.com/9cac9040-f652-4509-bbab-f2a41959d836">MESessionStopped</a> event.




## -see-also




<a href="https://msdn.microsoft.com/feebf891-73fa-4fe6-94ca-3594986fc92d">IMFMediaSession</a>
 

 

