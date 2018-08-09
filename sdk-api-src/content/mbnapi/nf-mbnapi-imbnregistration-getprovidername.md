---
UID: NF:mbnapi.IMbnRegistration.GetProviderName
title: IMbnRegistration::GetProviderName
author: windows-sdk-content
description: Gets the provider name for the currently registered network.
old-location: mbn\imbnregistration_getprovidername.htm
old-project: mbn
ms.assetid: c6cf7cb2-5563-49dc-ac2a-6343ae2395b2
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: GetProviderName, GetProviderName method [Microsoft Broadband Networks], GetProviderName method [Microsoft Broadband Networks],IMbnRegistration interface, IMbnRegistration interface [Microsoft Broadband Networks],GetProviderName method, IMbnRegistration.GetProviderName, IMbnRegistration::GetProviderName, mbn.imbnregistration_getprovidername, mbnapi/IMbnRegistration::GetProviderName
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mbnapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Mbnapi.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: MBN_VOICE_CLASS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mbnapi.h
api_name:
 - IMbnRegistration.GetProviderName
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMbnRegistration::GetProviderName


## -description


Gets the provider name for the currently registered network.


## -parameters




### -param providerName [out]

Pointer to a string that contains the name of the currently registered provider.  The maximum length of this string is <b>MBN_PROVIDERNAME_LEN</b> characters.  The string is filled only when the method returns <b>S_OK</b> for success.  Upon success, the calling application must free the allocated memory by calling <a href=" http://go.microsoft.com/fwlink/p/?linkid=120718">SysFreeString</a>.


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
The operation was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_PENDING</b></dt>
</dl>
</td>
<td width="60%">
The provider name is not available.  The Mobile Broadband service is currently probing the device for the information.  When the provider name is available, the Mobile Broadband service will call the <a href="https://msdn.microsoft.com/5c916f16-e8f5-4c8a-942c-3a9ae11905a7">OnRegisterModeAvailable</a> method of <a href="https://msdn.microsoft.com/f3b60a93-3b57-4c2c-9114-912ca47f16b2">IMbnRegistrationEvents</a>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_MBN_PIN_REQUIRED</b></dt>
</dl>
</td>
<td width="60%">
A PIN is required to get the provider name.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_MBN_SIM_NOT_INSERTED</b></dt>
</dl>
</td>
<td width="60%">
A SIM is not inserted in the device.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_MBN_BAD_SIM</b></dt>
</dl>
</td>
<td width="60%">
A bad SIM is inserted in the device.

</td>
</tr>
</table>
 




## -remarks



The provider name may change when the Mobile Broadband device moves from one network to another. This includes whenever there is change from <b>MBN_REGISTER_STATE_HOME</b> to <b>MBN_REGISTER_STATE_SEARCHING</b> in the network registration state.  This also occurs when there is a change in the registered network, such as when a  network changes its registration from one provider to another.  After such changes, the Mobile Broadband service will call the  <a href="https://msdn.microsoft.com/62393a9b-70e5-4819-8df1-59b94c1b6922">OnRegisterStateChange</a> method of <a href="https://msdn.microsoft.com/f3b60a93-3b57-4c2c-9114-912ca47f16b2">IMbnRegistrationEvents</a>. When this happens, the application should call <a href="https://msdn.microsoft.com/0b21a103-2b49-4d99-8041-c9da9cbc5750">GetProviderID</a>.

For the recoverable error <b>E_MBN_PIN_REQUIRED</b>, the Mobile Broadband service will try to refetch this information from the device when the error condition is over (when a PIN is entered).  Then it will call the  <a href="https://msdn.microsoft.com/62393a9b-70e5-4819-8df1-59b94c1b6922">OnRegisterStateChange</a> method of <a href="https://msdn.microsoft.com/f3b60a93-3b57-4c2c-9114-912ca47f16b2">IMbnRegistrationEvents</a>.





## -see-also




<a href="https://msdn.microsoft.com/da5413b7-adf4-4a3d-893f-f51441460541">IMbnRegistration</a>
 

 

