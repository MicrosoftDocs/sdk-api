---
UID: NF:tapi3if.ITBasicCallControl.BlindTransfer
title: ITBasicCallControl::BlindTransfer
author: windows-sdk-content
description: The BlindTransfer method performs a blind or single-step transfer of the specified call to the specified destination address. The application must be the owner of the call. After a successful transfer, the call state transitions to CS_DISCONNECTED.
old-location: tapi3\itbasiccallcontrol_blindtransfer.htm
tech.root: TAPI
ms.assetid: 766a48af-512a-4ad6-99e1-436141bf8447
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: BlindTransfer, BlindTransfer method [TAPI 2.2], BlindTransfer method [TAPI 2.2],ITBasicCallControl interface, ITBasicCallControl interface [TAPI 2.2],BlindTransfer method, ITBasicCallControl.BlindTransfer, ITBasicCallControl::BlindTransfer, _tapi3_itbasiccallcontrol_blindtransfer, tapi3.itbasiccallcontrol_blindtransfer, tapi3if/ITBasicCallControl::BlindTransfer
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
 - ITBasicCallControl.BlindTransfer
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITBasicCallControl::BlindTransfer


## -description


The 
<b>BlindTransfer</b> method performs a blind or single-step transfer of the specified call to the specified destination address. The application must be the owner of the call. After a successful transfer, the 
<a href="https://msdn.microsoft.com/d4ed5e99-3abe-4434-9f99-5e98d8c6f3f1">call state</a> transitions to CS_DISCONNECTED.


## -parameters




### -param pDestAddress [in]

Pointer to <b>BSTR</b> containing destination address for the transfer.


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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>pDestAddress</i> is not a valid pointer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
Blind transfer is not supported.

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

The application must use 
<a href="9e0437a2-9b4a-4576-88b0-5cb9d08ca29b">SysAllocString</a> to allocate memory for the <i>pDestAddress</i> parameter and use 
<a href="8f230ee3-5f6e-4cb9-a910-9c90b754dcd3">SysFreeString</a> to free the memory when the variable is no longer needed.

In some cases, the application may need to use the address translation interfaces (
<a href="https://msdn.microsoft.com/e1cd88f1-1ed7-4e7f-a745-9a9c4af69317">ITAddressTranslation</a> and 
<a href="https://msdn.microsoft.com/b59454a0-315f-4160-b969-d930c13bb4de">ITAddressTranslationInfo</a>) to obtain a <i>pDestAddress</i> string in the proper format.




## -see-also




<a href="https://msdn.microsoft.com/67c063ba-8b12-40d6-9011-923bdee8b214">Call Object</a>



<a href="https://msdn.microsoft.com/e1cd88f1-1ed7-4e7f-a745-9a9c4af69317">ITAddressTranslation</a>



<a href="https://msdn.microsoft.com/b59454a0-315f-4160-b969-d930c13bb4de">ITAddressTranslationInfo</a>



<a href="https://msdn.microsoft.com/a0b4c496-5ee8-4810-8170-8ea505c99f18">ITBasicCallControl</a>



<a href="https://msdn.microsoft.com/b1027f09-74e1-4da8-b718-bb55a56dda1d">Transfer Overview</a>



<a href="https://msdn.microsoft.com/c1997933-475e-4bcd-be44-ad92a2a678eb">lineBlindTransfer</a>
 

 

