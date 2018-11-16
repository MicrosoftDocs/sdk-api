---
UID: NF:tapi3if.ITBasicCallControl.RemoveFromConference
title: ITBasicCallControl::RemoveFromConference
author: windows-sdk-content
description: The RemoveFromConference method removes the call from a conference if it is involved in one.
old-location: tapi3\itbasiccallcontrol_removefromconference.htm
tech.root: Tapi
ms.assetid: c3a357a1-9bfa-4d23-b7d7-e1d9b636e861
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: ITBasicCallControl interface [TAPI 2.2],RemoveFromConference method, ITBasicCallControl.RemoveFromConference, ITBasicCallControl::RemoveFromConference, RemoveFromConference, RemoveFromConference method [TAPI 2.2], RemoveFromConference method [TAPI 2.2],ITBasicCallControl interface, _tapi3_itbasiccallcontrol_removefromconference, tapi3.itbasiccallcontrol_removefromconference, tapi3if/ITBasicCallControl::RemoveFromConference
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tapi3.dll
api_name:
 - ITBasicCallControl.RemoveFromConference
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- tapi3if.h
: 
- ITBasicCallControl.RemoveFromConference
: 
---

# ITBasicCallControl::RemoveFromConference


## -description


The 
<b>RemoveFromConference</b> method removes the call from a conference if it is involved in one.


## -parameters






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
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory exists to perform the operation.

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
</table>
 




## -remarks



Some service providers do not support this operation while streaming is active. The application may need to call 
<a href="https://msdn.microsoft.com/6014e76e-ce2c-4ab8-b6f2-c09fc2acf315">ITStream::StopStream</a> or 
<a href="https://msdn.microsoft.com/fa5028f6-80eb-4076-a81c-c83b462fc27c">ITSubStream::StopSubStream</a> prior to the operation and 
<a href="https://msdn.microsoft.com/23553f00-5ce5-465e-b455-8bf2d73dae9d">ITStream::StartStream</a> or 
<a href="https://msdn.microsoft.com/603cb667-a108-4e47-9808-99fddad5d894">ITSubStream::StartSubStream</a> following completion of the operation.




## -see-also




<a href="https://msdn.microsoft.com/67c063ba-8b12-40d6-9011-923bdee8b214">Call Object</a>



<a href="https://msdn.microsoft.com/f685097b-1b54-412b-999f-d9bdb3120ab9">Conference overview</a>



<a href="https://msdn.microsoft.com/a0b4c496-5ee8-4810-8170-8ea505c99f18">ITBasicCallControl</a>



<a href="https://msdn.microsoft.com/03363579-66c2-4bb5-b110-01084c20bf09">lineRemoveFromConference</a>
 

 

