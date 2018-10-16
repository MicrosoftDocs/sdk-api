---
UID: NF:mfidl.IMFMediaSession.Shutdown
title: IMFMediaSession::Shutdown
author: windows-sdk-content
description: Shuts down the Media Session and releases all the resources used by the Media Session.
old-location: mf\imfmediasession_shutdown.htm
tech.root: medfound
ms.assetid: 5b9663c2-e32e-4075-b397-59ae01558e15
ms.author: windowssdkdev
ms.date: 10/15/2018
ms.keywords: 5b9663c2-e32e-4075-b397-59ae01558e15, IMFMediaSession interface [Media Foundation],Shutdown method, IMFMediaSession.Shutdown, IMFMediaSession::Shutdown, Shutdown, Shutdown method [Media Foundation], Shutdown method [Media Foundation],IMFMediaSession interface, mf.imfmediasession_shutdown, mfidl/IMFMediaSession::Shutdown
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
 - IMFMediaSession.Shutdown
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFMediaSession::Shutdown


## -description



Shuts down the Media Session and releases all the resources used by the Media Session.




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
</table>
 




## -remarks



Call this method when you are done using the Media Session, before the final call to <b>IUnknown::Release</b>. Otherwise, your application will leak memory.

After this method is called, other <a href="https://msdn.microsoft.com/feebf891-73fa-4fe6-94ca-3594986fc92d">IMFMediaSession</a> methods return MF_E_SHUTDOWN.




## -see-also




<a href="https://msdn.microsoft.com/feebf891-73fa-4fe6-94ca-3594986fc92d">IMFMediaSession</a>
 

 

