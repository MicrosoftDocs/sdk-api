---
UID: NF:control.IDeferredCommand.Postpone
title: IDeferredCommand::Postpone
author: windows-sdk-content
description: The Postpone method specifies a new invocation time for the command.
old-location: dshow\ideferredcommand_postpone.htm
tech.root: DirectShow
ms.assetid: 184370db-95df-45a8-b1a0-e399923f866e
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IDeferredCommand interface [DirectShow],Postpone method, IDeferredCommand.Postpone, IDeferredCommand::Postpone, IDeferredCommandPostpone, Postpone, Postpone method [DirectShow], Postpone method [DirectShow],IDeferredCommand interface, control/IDeferredCommand::Postpone, dshow.ideferredcommand_postpone
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: control.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Strmiids.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IDeferredCommand.Postpone
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDeferredCommand::Postpone


## -description



The <code>Postpone</code> method specifies a new invocation time for the command.




## -parameters




### -param newtime

New time at which to invoke the command.


## -returns



Returns an <b>HRESULT</b> value. Possible values include the following.

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
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_TIME_ALREADY_PASSED</b></dt>
</dl>
</td>
<td width="60%">
The specified time has already passed.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd375623(v=VS.85).aspx">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd406762(v=VS.85).aspx">IDeferredCommand Interface</a>
 

 

