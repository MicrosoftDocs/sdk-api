---
UID: NF:mfidl.IMFMediaSession.GetClock
title: IMFMediaSession::GetClock
author: windows-driver-content
description: Retrieves the Media Session's presentation clock.
old-location: mf\imfmediasession_getclock.htm
old-project: medfound
ms.assetid: 16444da2-68f2-4d94-8c6f-9e512d51e5e9
ms.author: windowsdriverdev
ms.date: 5/18/2018
ms.keywords: 16444da2-68f2-4d94-8c6f-9e512d51e5e9, GetClock, GetClock method [Media Foundation], GetClock method [Media Foundation],IMFMediaSession interface, IMFMediaSession interface [Media Foundation],GetClock method, IMFMediaSession.GetClock, IMFMediaSession::GetClock, mf.imfmediasession_getclock, mfidl/IMFMediaSession::GetClock
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
-	IMFMediaSession.GetClock
product: Windows
targetos: Windows
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFMediaSession::GetClock


## -description



Retrieves the Media Session's presentation clock.




## -parameters




### -param ppClock [out]

Receives a pointer to the presentation clock's <a href="https://msdn.microsoft.com/3a60bfec-8511-4a84-a833-e0c73c593970">IMFClock</a> interface. The caller must release the interface.


## -returns



The method returns an HRESULT. Possible values include, but are not limited to, those in the following table.

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
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
The Media Session does not have a presentation clock.

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



The application can query the returned <a href="https://msdn.microsoft.com/3a60bfec-8511-4a84-a833-e0c73c593970">IMFClock</a> pointer for the <a href="https://msdn.microsoft.com/979c4f77-cbee-468c-8f6b-e68442d89025">IMFPresentationClock</a> interface. However, the application should not use this interface to control the state of the presentation clock. Instead, the application should always call the transport control methods on the Media Session's <a href="https://msdn.microsoft.com/feebf891-73fa-4fe6-94ca-3594986fc92d">IMFMediaSession</a> interface, such as <a href="https://msdn.microsoft.com/library/windows/hardware/hh973223">Start</a>, <a href="https://msdn.microsoft.com/library/windows/hardware/dn927275">Stop</a>, and <a href="https://msdn.microsoft.com/library/windows/hardware/hh451189">Pause</a>.




## -see-also




<a href="https://msdn.microsoft.com/feebf891-73fa-4fe6-94ca-3594986fc92d">IMFMediaSession</a>
 

 

