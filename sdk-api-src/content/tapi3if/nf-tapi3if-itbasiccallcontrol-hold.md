---
UID: NF:tapi3if.ITBasicCallControl.Hold
title: ITBasicCallControl::Hold (tapi3if.h)
author: windows-sdk-content
description: The Hold method places or removes the call from the hold.
old-location: tapi3\itbasiccallcontrol_hold.htm
tech.root: Tapi
ms.assetid: 44f1d3fd-6c48-41f4-a30e-83bf2ce19fde
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: Hold, Hold method [TAPI 2.2], Hold method [TAPI 2.2],ITBasicCallControl interface, ITBasicCallControl interface [TAPI 2.2],Hold method, ITBasicCallControl.Hold, ITBasicCallControl::Hold, _tapi3_itbasiccallcontrol_hold, tapi3.itbasiccallcontrol_hold, tapi3if/ITBasicCallControl::Hold
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
 - ITBasicCallControl.Hold
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITBasicCallControl::Hold


## -description


The 
<b>Hold</b> method places or removes the call from the hold.


## -parameters




### -param fHold [in]

If <i>fHold</i> is VARIANT_TRUE and the method succeeds, the 
<a href="https://msdn.microsoft.com/d4ed5e99-3abe-4434-9f99-5e98d8c6f3f1">call state</a> transitions to the CS_HOLD state. If <i>fHold</i> is VARIANT_FALSE, the call state transitions to CS_CONNECTED.


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
<dt><b>TAPI_E_INVALCALLSTATE</b></dt>
</dl>
</td>
<td width="60%">
The call associated with this interface no longer exists.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TAPI_E_TIMEOUT</b></dt>
</dl>
</td>
<td width="60%">
The operation failed because the TAPI 3 DLL timed it out. The timeout interval is two minutes

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



<a href="https://msdn.microsoft.com/65e22e4e-e346-41c2-929a-ba0d1f7f1732">Hold overview</a>



<a href="https://msdn.microsoft.com/a0b4c496-5ee8-4810-8170-8ea505c99f18">ITBasicCallControl</a>



<a href="https://msdn.microsoft.com/d2fd450c-402c-4122-a785-a6b5216acfe9">lineHold</a>
 

 

