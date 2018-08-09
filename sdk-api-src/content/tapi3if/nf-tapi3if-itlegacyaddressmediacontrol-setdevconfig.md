---
UID: NF:tapi3if.ITLegacyAddressMediaControl.SetDevConfig
title: ITLegacyAddressMediaControl::SetDevConfig
author: windows-sdk-content
description: The SetDevConfig function allows the application to restore the configuration of a media stream device on a line device to a setup previously obtained using GetDevConfig.
old-location: tapi3\itlegacyaddressmediacontrol_setdevconfig.htm
old-project: tapi
ms.assetid: 7c5fe0ab-8a03-41db-994b-9786782cf7c1
ms.author: windowssdkdev
ms.date: 07/31/2018
ms.keywords: ITLegacyAddressMediaControl interface [TAPI 2.2],SetDevConfig method, ITLegacyAddressMediaControl.SetDevConfig, ITLegacyAddressMediaControl::SetDevConfig, SetDevConfig, SetDevConfig method [TAPI 2.2], SetDevConfig method [TAPI 2.2],ITLegacyAddressMediaControl interface, _tapi3_itlegacyaddressmediacontrol_setdevconfig, tapi3.itlegacyaddressmediacontrol_setdevconfig, tapi3if/ITLegacyAddressMediaControl::SetDevConfig
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
 - ITLegacyAddressMediaControl.SetDevConfig
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITLegacyAddressMediaControl::SetDevConfig


## -description


The 
<b>SetDevConfig</b> function allows the application to restore the configuration of a media stream device on a line device to a setup previously obtained using 
<a href="https://msdn.microsoft.com/ed8cc556-31a5-4725-92fe-1f78c16aadcd">GetDevConfig</a>.


## -parameters




### -param pDeviceClass [in]

Pointer to <b>BSTR</b> containing 
<a href="https://msdn.microsoft.com/859979a8-0d16-4b7b-b183-d6e30f3e034d">TAPI device class</a> for which configuration information is needed.


### -param dwSize [in]

Size of configuration array.


### -param pDeviceConfig [in]

Pointer to the array of bytes containing device configuration information obtained by a call to 
<a href="https://msdn.microsoft.com/ed8cc556-31a5-4725-92fe-1f78c16aadcd">GetDevConfig</a>.


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
The <i>pDeviceClass</i>, <i>pdwSize</i>, or <i>ppDeviceConfig</i> parameter is not a valid pointer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>pdwSize</i> parameter is zero.

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



This method is a COM wrapper for the 
<a href="https://msdn.microsoft.com/f1b04224-e535-4100-b026-3203eebc42c8">lineSetDevConfig</a> TAPI 2.1 function.

The 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff546827">GetID</a> must be performed prior to calling this method.

The application must use 
<a href="https://msdn.microsoft.com/en-us/library/ms221458(v=VS.85).aspx">SysAllocString</a> to allocate memory for the <i>pDeviceClass</i> parameter and use 
<a href="https://msdn.microsoft.com/en-us/library/ms221481(v=VS.85).aspx">SysFreeString</a> to free the memory when the variable is no longer needed.

<b>TAPI 2.1 Cross-References:  </b><a href="https://msdn.microsoft.com/39ff5ddb-142e-4f11-9395-e2c3a3ac7d19">lineGetDevConfig</a>, <a href="https://msdn.microsoft.com/f1b04224-e535-4100-b026-3203eebc42c8">lineSetDevConfig</a>





## -see-also




<a href="https://msdn.microsoft.com/ed8cc556-31a5-4725-92fe-1f78c16aadcd">GetDevConfig</a>



<a href="https://msdn.microsoft.com/5f3d0189-fc9d-4fa5-bc8e-a0abf1f607f8">ITLegacyAddressMediaControl</a>



<a href="https://msdn.microsoft.com/73288c46-6c6d-4938-9bb7-4d94acfc67f6">ITLegacyCallMediaControl</a>
 

 

