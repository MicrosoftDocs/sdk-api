---
UID: NF:wmsdkidl.IWMDeviceRegistration.GetRegistrationStats
title: IWMDeviceRegistration::GetRegistrationStats
author: windows-sdk-content
description: The GetRegistrationStats method retrieves the number of devices in the device registration database that have a specified type.
old-location: wmformat\iwmdeviceregistration_getregistrationstats.htm
old-project: wmformat
ms.assetid: 56c5b2c7-46c2-42e4-a7d4-f1b3e56ffbcb
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: GetRegistrationStats, GetRegistrationStats method [windows Media Format], GetRegistrationStats method [windows Media Format],IWMDeviceRegistration interface, IWMDeviceRegistration interface [windows Media Format],GetRegistrationStats method, IWMDeviceRegistration.GetRegistrationStats, IWMDeviceRegistration::GetRegistrationStats, IWMDeviceRegistrationGetRegistrationStats, wmformat.iwmdeviceregistration_getregistrationstats, wmsdkidl/IWMDeviceRegistration::GetRegistrationStats
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wmsdkidl.h
req.include-header: Wmsdk.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only],Windows Media Format 9.5 SDK
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: WM_AETYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	WMStubDRM.lib
-	WMStubDRM.dll
api_name:
-	IWMDeviceRegistration.GetRegistrationStats
product: Windows
targetos: Windows
req.lib: WMStubDRM.lib
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMDeviceRegistration::GetRegistrationStats


## -description


<p class="CCE_Message">[<b>GetRegistrationStats</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="http://go.microsoft.com/fwlink/p/?linkid=325240">Microsoft PlayReady</a>.
]


The <b>GetRegistrationStats</b> method retrieves the number of devices in the device registration database that have a specified type.




## -parameters




### -param dwRegisterType [in]

The type of the device for which to retrieve the count. Devices that support Windows Media DRM 10 for Network Devices use the DRM_DEVICE_REGISTER_TYPE_STREAMING register type.


### -param pcRegisteredDevices [out]

Address of a variable that receives the number of registered devices of the specified type.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

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
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>pcRegisteredDevices</i> parameter is <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



The DRM_DEVICE_REGISTER_TYPE_STORAGE register type is defined, but is not used in this release.




## -see-also




<a href="https://msdn.microsoft.com/fb08ddae-2abf-4a86-a5d8-ea745ae35aa8">IWMDeviceRegistration Interface</a>
 

 

