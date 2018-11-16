---
UID: NF:sensevts.ISensLogon.StopScreenSaver
title: ISensLogon::StopScreenSaver
author: windows-sdk-content
description: The StopScreenSaver method notifies an application that a screen saver is stopped.
old-location: sens\isenslogon_stopscreensaver.htm
tech.root: Sens
ms.assetid: 61a6434b-1a80-4a37-9175-636c3792a865
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: ISensLogon interface [SENS],StopScreenSaver method, ISensLogon.StopScreenSaver, ISensLogon::StopScreenSaver, StopScreenSaver, StopScreenSaver method [SENS], StopScreenSaver method [SENS],ISensLogon interface, _zaw_isenslogon_stopscreensaver, sens.isenslogon_stopscreensaver, sensevts/ISensLogon::StopScreenSaver, syncmgr.isenslogon_stopscreensaver
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: sensevts.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: Sensevts.tlb
req.lib: 
req.dll: Sens.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Sens.dll
api_name:
 - ISensLogon.StopScreenSaver
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- sensevts.h
: 
- ISensLogon.StopScreenSaver
: 
---

# ISensLogon::StopScreenSaver


## -description


The 
<b>StopScreenSaver</b> method notifies an application that a screen saver is stopped.


## -parameters




### -param bstrUserName [in]

The name of a current user.


## -returns



This method can return one of these values.

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
The method returns successfully.

</td>
</tr>
</table>
 




## -remarks



SENS calls this method to notify an application that a screen saver is stopped.




## -see-also




<a href="https://msdn.microsoft.com/f313588f-6257-4a0d-b95a-aabc0bc64b53">About System Event Notification Service</a>



<a href="_cos_ieventsubscription">IEventSubscription</a>



<a href="_cos_ieventsubscription_putpublisherproperty">IEventSubscription::PutPublisherProperty</a>



<a href="https://msdn.microsoft.com/77c02510-6386-4f6d-af1a-e7337f5d347d">ISensLogon</a>



<a href="https://msdn.microsoft.com/1675ffc7-7031-492d-bf39-64281a16a074">ISensLogon::DisplayLock</a>



<a href="https://msdn.microsoft.com/aa1b1beb-f59a-4990-84e1-deca1432f6cf">ISensLogon::DisplayUnLock</a>



<a href="https://msdn.microsoft.com/47531e1f-e2d4-4475-a109-e213c903a7ba">ISensLogon::StartScreenSaver</a>
 

 

