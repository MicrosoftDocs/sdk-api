---
UID: NF:sensevts.ISensLogon.StartShell
title: ISensLogon::StartShell
author: windows-sdk-content
description: The StartShell method notifies an application that the shell is started.
old-location: sens\isenslogon_startshell.htm
tech.root: Sens
ms.assetid: 0bde3bda-c0ed-4303-b6c1-dd667e9b7504
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: ISensLogon interface [SENS],StartShell method, ISensLogon.StartShell, ISensLogon::StartShell, StartShell, StartShell method [SENS], StartShell method [SENS],ISensLogon interface, _zaw_isenslogon_startshell, sens.isenslogon_startshell, sensevts/ISensLogon::StartShell, syncmgr.isenslogon_startshell
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
 - ISensLogon.StartShell
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISensLogon::StartShell


## -description


The 
<b>StartShell</b> method notifies an application that the shell is started.


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



SENS calls this method to notify an application that the shell is started.




## -see-also




<a href="https://msdn.microsoft.com/f313588f-6257-4a0d-b95a-aabc0bc64b53">About System Event Notification Service</a>



<a href="https://msdn.microsoft.com/en-us/library/ms686510(v=VS.85).aspx">IEventSubscription</a>



<a href="https://msdn.microsoft.com/en-us/library/ms685465(v=VS.85).aspx">IEventSubscription::PutPublisherProperty</a>



<a href="https://msdn.microsoft.com/77c02510-6386-4f6d-af1a-e7337f5d347d">ISensLogon</a>
 

 

