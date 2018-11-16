---
UID: NF:tapi3if.ITBasicCallControl.Dial
title: ITBasicCallControl::Dial
author: windows-sdk-content
description: The Dial method dials the specified address.
old-location: tapi3\itbasiccallcontrol_dial.htm
tech.root: Tapi
ms.assetid: 31fea4d8-9028-48d5-9f5d-53f1451103c7
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: Dial, Dial method [TAPI 2.2], Dial method [TAPI 2.2],ITBasicCallControl interface, ITBasicCallControl interface [TAPI 2.2],Dial method, ITBasicCallControl.Dial, ITBasicCallControl::Dial, _tapi3_itbasiccallcontrol_dial, tapi3.itbasiccallcontrol_dial, tapi3if/ITBasicCallControl::Dial
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
 - ITBasicCallControl.Dial
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
- ITBasicCallControl.Dial
: 
---

# ITBasicCallControl::Dial


## -description


The 
<b>Dial</b> method dials the specified address.


## -parameters




### -param pDestAddress [in]

Pointer to <b>BSTR</b> representation of address to be dialed. The format must conform to a standard 
<a href="address_ovr.htm">dialable address</a>.


## -returns



This method can return one of these values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>pDestAddress</i> parameter is not a valid pointer.

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



The application must use 
<a href="9e0437a2-9b4a-4576-88b0-5cb9d08ca29b">SysAllocString</a> to allocate memory for the <i>pDestAddress</i> parameter and use 
<a href="8f230ee3-5f6e-4cb9-a910-9c90b754dcd3">SysFreeString</a> to free the memory when the variable is no longer needed.

In some cases, the application may need to use the address translation interfaces (
<a href="https://msdn.microsoft.com/e1cd88f1-1ed7-4e7f-a745-9a9c4af69317">ITAddressTranslation</a> and 
<a href="https://msdn.microsoft.com/b59454a0-315f-4160-b969-d930c13bb4de">ITAddressTranslationInfo</a>) to obtain a <i>pDestAddress</i> string in the proper format.

The 
<b>Dial</b> method differs from 
<a href="https://msdn.microsoft.com/1b5a755c-fdaf-42ca-9747-9b34efbd0ac3">ITAddress::CreateCall</a> in that the call already exists. An example use is dialing an extension.




## -see-also




<a href="https://msdn.microsoft.com/67c063ba-8b12-40d6-9011-923bdee8b214">Call Object</a>



<a href="https://msdn.microsoft.com/1dfaefd7-f8dd-451e-af18-249c89bdb517">Dial overview</a>



<a href="address_ovr.htm">Dialable Addresses</a>



<a href="https://msdn.microsoft.com/1b5a755c-fdaf-42ca-9747-9b34efbd0ac3">ITAddress::CreateCall</a>



<a href="https://msdn.microsoft.com/e1cd88f1-1ed7-4e7f-a745-9a9c4af69317">ITAddressTranslation</a>



<a href="https://msdn.microsoft.com/b59454a0-315f-4160-b969-d930c13bb4de">ITAddressTranslationInfo</a>



<a href="https://msdn.microsoft.com/a0b4c496-5ee8-4810-8170-8ea505c99f18">ITBasicCallControl</a>



<a href="https://msdn.microsoft.com/111e6c11-67a7-4aab-81dd-f1b4316887e7">lineDial</a>
 

 

