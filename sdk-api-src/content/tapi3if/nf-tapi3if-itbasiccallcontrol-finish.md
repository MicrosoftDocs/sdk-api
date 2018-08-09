---
UID: NF:tapi3if.ITBasicCallControl.Finish
title: ITBasicCallControl::Finish
author: windows-sdk-content
description: The Finish method is called on a consultation call to finish a conference or a transfer.
old-location: tapi3\itbasiccallcontrol_finish.htm
old-project: tapi
ms.assetid: 3b0bd871-b618-4c24-a717-62a248112d97
ms.author: windowssdkdev
ms.date: 07/31/2018
ms.keywords: Finish, Finish method [TAPI 2.2], Finish method [TAPI 2.2],ITBasicCallControl interface, ITBasicCallControl interface [TAPI 2.2],Finish method, ITBasicCallControl.Finish, ITBasicCallControl::Finish, _tapi3_itbasiccallcontrol_finish, tapi3.itbasiccallcontrol_finish, tapi3if/ITBasicCallControl::Finish
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: tapi3if.h
req.include-header: Tapi3.h
req.target-type: Windows
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
tech.root: 
req.typenames: TERMINAL_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tapi3.dll
api_name:
 - ITBasicCallControl.Finish
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITBasicCallControl::Finish


## -description


The 
<b>Finish</b> method is called on a consultation call to finish a conference or a transfer.


## -parameters




### -param finishMode [in]

A 
<a href="https://msdn.microsoft.com/f0bf1d93-b6c3-473a-b7ee-2ebb984f42c5">FINISH_MODE</a> indicator of the type of call being finished, such as FM_ASCONFERENCE.


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
Method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TAPI_E_INVALCALLSTATE</b></dt>
</dl>
</td>
<td width="60%">
Call is not flagged as a transfer or a conference.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TAPI_E_TIMEOUT</b></dt>
</dl>
</td>
<td width="60%">
The operation failed because the TAPI 3 DLL timed it out. The timeout interval is two minutes.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory exists to perform the operation.

</td>
</tr>
</table>
 




## -remarks



Some service providers do not support this operation while streaming is active. The application may need to call 
<a href="https://msdn.microsoft.com/6014e76e-ce2c-4ab8-b6f2-c09fc2acf315">ITStream::StopStream</a> or 
<a href="https://msdn.microsoft.com/fa5028f6-80eb-4076-a81c-c83b462fc27c">ITSubStream::StopSubStream</a> prior to the operation and 
<a href="https://msdn.microsoft.com/23553f00-5ce5-465e-b455-8bf2d73dae9d">ITStream::StartStream</a> or 
<a href="https://msdn.microsoft.com/603cb667-a108-4e47-9808-99fddad5d894">ITSubStream::StartSubStream</a> following completion of the operation.




## -see-also




<a href="https://msdn.microsoft.com/67c063ba-8b12-40d6-9011-923bdee8b214">Call Object</a>



<a href="https://msdn.microsoft.com/73721921-c943-4adc-a2b1-e8c19ec809ac">Conference</a>



<a href="https://msdn.microsoft.com/f685097b-1b54-412b-999f-d9bdb3120ab9">Conference overview</a>



<a href="https://msdn.microsoft.com/fb55853d-b882-41c8-99e6-bfa897b2dabf">Create a Simple Conference code snippet</a>



<a href="https://msdn.microsoft.com/f0bf1d93-b6c3-473a-b7ee-2ebb984f42c5">FINISH_MODE</a>



<a href="https://msdn.microsoft.com/c70bf596-b2a4-46ec-9b1a-c9d948768b51">Forward overview</a>



<a href="https://msdn.microsoft.com/a0b4c496-5ee8-4810-8170-8ea505c99f18">ITBasicCallControl</a>



<a href="https://msdn.microsoft.com/4f2a06e6-9f0b-4bf3-9f18-6e9f57c4b02f">Transfer</a>



<a href="https://msdn.microsoft.com/b1027f09-74e1-4da8-b718-bb55a56dda1d">Transfer overview</a>
 

 

