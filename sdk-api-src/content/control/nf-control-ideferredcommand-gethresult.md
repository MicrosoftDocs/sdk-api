---
UID: NF:control.IDeferredCommand.GetHResult
title: IDeferredCommand::GetHResult
author: windows-sdk-content
description: The GetHResult method retrieves the return value from the invoked command.
old-location: dshow\ideferredcommand_gethresult.htm
tech.root: DirectShow
ms.assetid: ce047464-d283-4ff4-a5eb-9e394d4ac3fd
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: GetHResult, GetHResult method [DirectShow], GetHResult method [DirectShow],IDeferredCommand interface, IDeferredCommand interface [DirectShow],GetHResult method, IDeferredCommand.GetHResult, IDeferredCommand::GetHResult, IDeferredCommandGetHResult, control/IDeferredCommand::GetHResult, dshow.ideferredcommand_gethresult
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
 - IDeferredCommand.GetHResult
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDeferredCommand::GetHResult


## -description



The <code>GetHResult</code> method retrieves the return value from the invoked command.




## -parameters




### -param phrResult

Receives the <b>HRESULT</b> value.


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
<dt><b>E_ABORT</b></dt>
</dl>
</td>
<td width="60%">
Command has not yet been invoked.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<b>NULL</b> pointer argument.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd375623(v=VS.85).aspx">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd406762(v=VS.85).aspx">IDeferredCommand Interface</a>
 

 

