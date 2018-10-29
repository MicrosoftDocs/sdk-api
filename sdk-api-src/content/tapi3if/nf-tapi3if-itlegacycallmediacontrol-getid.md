---
UID: NF:tapi3if.ITLegacyCallMediaControl.GetID
title: ITLegacyCallMediaControl::GetID
author: windows-sdk-content
description: The GetID method gets the identifier for the device associated with the current call.
old-location: tapi3\itlegacycallmediacontrol_getid.htm
tech.root: Tapi
ms.assetid: 7516f929-d782-499b-a9fb-24c44a85aa9e
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: GetID, GetID method [TAPI 2.2], GetID method [TAPI 2.2],ITLegacyCallMediaControl interface, ITLegacyCallMediaControl interface [TAPI 2.2],GetID method, ITLegacyCallMediaControl.GetID, ITLegacyCallMediaControl::GetID, _tapi3_itlegacycallmediacontrol_getid, tapi3.itlegacycallmediacontrol_getid, tapi3if/ITLegacyCallMediaControl::GetID
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
 - ITLegacyCallMediaControl.GetID
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITLegacyCallMediaControl::GetID


## -description


The 
<b>GetID</b> method gets the identifier for the device associated with the current call.

This method is intended for C/C++ applications.  Visual Basic and scripting applications should use the 
<a href="https://msdn.microsoft.com/6c28889f-3768-4136-ac73-80c6c5ffeac3">ITLegacyCallMediaControl2::GetIDAsVariant</a> method.


## -parameters




### -param pDeviceClass [in]

Pointer to <b>BSTR</b> representing the 
<a href="https://msdn.microsoft.com/859979a8-0d16-4b7b-b183-d6e30f3e034d">TAPI device class</a>.


### -param pdwSize [out]

Size in bytes of device identifier.


### -param ppDeviceID [out]

Device identifier.


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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>pdwSize</i> or <i>ppDeviceID</i> parameter is not a valid pointer.

</td>
</tr>
</table>
 




## -remarks



The application must call 
<a href="https://msdn.microsoft.com/335deb2c-7700-4101-b6fa-f7fe0f248307">ITTAPI::RegisterCallNotifications</a> prior to calling this method.

The application must use 
<a href="9e0437a2-9b4a-4576-88b0-5cb9d08ca29b">SysAllocString</a> to allocate memory for the <i>pDeviceClass</i> parameter and use 
<a href="8f230ee3-5f6e-4cb9-a910-9c90b754dcd3">SysFreeString</a> to free the memory when the variable is no longer needed.

The application must call the 
<a href="https://msdn.microsoft.com/en-us/library/windows/desktop/ms680722">CoTaskMemFree</a> function to free the memory allocated for the <i>ppDeviceID</i> parameter.




## -see-also




<a href="https://msdn.microsoft.com/5f3d0189-fc9d-4fa5-bc8e-a0abf1f607f8">ITLegacyAddressMediaControl</a>



<a href="https://msdn.microsoft.com/73288c46-6c6d-4938-9bb7-4d94acfc67f6">ITLegacyCallMediaControl</a>



<a href="https://msdn.microsoft.com/6c28889f-3768-4136-ac73-80c6c5ffeac3">ITLegacyCallMediaControl2::GetIDAsVariant</a>
 

 

