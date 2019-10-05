---
UID: NF:mfidl.IMFMediaSession.Stop
title: IMFMediaSession::Stop (mfidl.h)
author: windows-sdk-content
description: Stops the Media Session.
old-location: mf\imfmediasession_stop.htm
tech.root: medfound
ms.assetid: 9cc769cc-24ef-4790-a10e-4aec8fb4fc1f
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: 9cc769cc-24ef-4790-a10e-4aec8fb4fc1f, IMFMediaSession interface [Media Foundation],Stop method, IMFMediaSession.Stop, IMFMediaSession::Stop, Stop, Stop method [Media Foundation], Stop method [Media Foundation],IMFMediaSession interface, mf.imfmediasession_stop, mfidl/IMFMediaSession::Stop
ms.topic: method
f1_keywords: 
 - "mfidl/IMFMediaSession.Stop"
dev_langs:
 - c++
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
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFMediaSession.Stop
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFMediaSession::Stop


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



This method is asynchronous. When the operation completes, the Media Session sends an <a href="https://docs.microsoft.com/windows/desktop/medfound/mesessionstopped">MESessionStopped</a> event.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nn-mfidl-imfmediasession">IMFMediaSession</a>
 

 

