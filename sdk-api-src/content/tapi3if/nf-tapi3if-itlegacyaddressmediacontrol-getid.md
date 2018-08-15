---
UID: NF:tapi3if.ITLegacyAddressMediaControl.GetID
title: ITLegacyAddressMediaControl::GetID
author: windows-sdk-content
description: The GetID method returns a device identifier for the specified device class associated with the current address.
old-location: tapi3\itlegacyaddressmediacontrol_getid.htm
old-project: tapi
ms.assetid: f4fdde49-0867-4967-b975-f43bd9f6adc4
ms.author: windowssdkdev
ms.date: 07/31/2018
ms.keywords: GetID, GetID method [TAPI 2.2], GetID method [TAPI 2.2],ITLegacyAddressMediaControl interface, ITLegacyAddressMediaControl interface [TAPI 2.2],GetID method, ITLegacyAddressMediaControl.GetID, ITLegacyAddressMediaControl::GetID, _tapi3_itlegacyaddressmediacontrol_getid, tapi3.itlegacyaddressmediacontrol_getid, tapi3if/ITLegacyAddressMediaControl::GetID
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: tapi3if.h
req.include-header: Tapi3.h
req.redist: 
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
 - ITLegacyAddressMediaControl.GetID
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITLegacyAddressMediaControl::GetID


## -description


The 
<b>GetID</b> method returns a device identifier for the specified device class associated with the current address.

This method is intended for C/C++ applications only. There is no corresponding method available for Visual Basic and scripting applications.


## -parameters




### -param pDeviceClass [in]

Pointer to <b>BSTR</b> containing 
<a href="https://msdn.microsoft.com/859979a8-0d16-4b7b-b183-d6e30f3e034d">TAPI device class</a> for which configuration information is needed.


### -param pdwSize [out]

Length of device identifier returned.


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
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
Method failed. This may mean there is no device of a specified class associated with the current address.

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
<a href="https://msdn.microsoft.com/en-us/library/ms221458(v=VS.85).aspx">SysAllocString</a> to allocate memory for the <i>pDeviceClass</i> parameter and use 
<a href="https://msdn.microsoft.com/en-us/library/ms221481(v=VS.85).aspx">SysFreeString</a> to free the memory when the variable is no longer needed.

The application must call the 
<a href="https://msdn.microsoft.com/en-us/library/windows/desktop/ms680722">CoTaskMemFree</a> function to free the memory allocated for the <i>ppDeviceID</i> parameter.

<b>TAPI 2.1 Cross-References:  </b><a href="https://msdn.microsoft.com/39ff5ddb-142e-4f11-9395-e2c3a3ac7d19">lineGetDevConfig</a>, <a href="https://msdn.microsoft.com/f1b04224-e535-4100-b026-3203eebc42c8">lineSetDevConfig</a>, <a href="https://msdn.microsoft.com/e9981574-0058-420f-9627-6d5a1745a739">lineGetID</a>





## -see-also




<a href="https://msdn.microsoft.com/ed8cc556-31a5-4725-92fe-1f78c16aadcd">GetDevConfig</a>



<a href="https://msdn.microsoft.com/5f3d0189-fc9d-4fa5-bc8e-a0abf1f607f8">ITLegacyAddressMediaControl</a>



<a href="https://msdn.microsoft.com/73288c46-6c6d-4938-9bb7-4d94acfc67f6">ITLegacyCallMediaControl</a>



<a href="https://msdn.microsoft.com/7c5fe0ab-8a03-41db-994b-9786782cf7c1">SetDevConfig</a>
 

 

