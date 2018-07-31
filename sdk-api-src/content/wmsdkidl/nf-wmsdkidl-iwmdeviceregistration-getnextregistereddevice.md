---
UID: NF:wmsdkidl.IWMDeviceRegistration.GetNextRegisteredDevice
title: IWMDeviceRegistration::GetNextRegisteredDevice
author: windows-sdk-content
description: The GetNextRegisteredDevice method enumerates the registered devices of a specified type.
old-location: wmformat\iwmdeviceregistration_getnextregistereddevice.htm
old-project: wmformat
ms.assetid: 396e60a8-5845-45fa-8393-6f0defbd38bb
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: GetNextRegisteredDevice, GetNextRegisteredDevice method [windows Media Format], GetNextRegisteredDevice method [windows Media Format],IWMDeviceRegistration interface, IWMDeviceRegistration interface [windows Media Format],GetNextRegisteredDevice method, IWMDeviceRegistration.GetNextRegisteredDevice, IWMDeviceRegistration::GetNextRegisteredDevice, IWMDeviceRegistrationGetNextRegisteredDevice, wmformat.iwmdeviceregistration_getnextregistereddevice, wmsdkidl/IWMDeviceRegistration::GetNextRegisteredDevice
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
tech.root: 
req.typenames: WM_AETYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - WMStubDRM.lib
 - WMStubDRM.dll
api_name:
 - IWMDeviceRegistration.GetNextRegisteredDevice
product: Windows
targetos: Windows
req.lib: WMStubDRM.lib
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMDeviceRegistration::GetNextRegisteredDevice


## -description


<p class="CCE_Message">[<b>GetNextRegisteredDevice</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="http://go.microsoft.com/fwlink/p/?linkid=325240">Microsoft PlayReady</a>.
]


The <b>GetNextRegisteredDevice</b> method enumerates the registered devices of a specified type.




## -parameters




### -param ppDevice [out]

Address of a variable that receives a pointer to an <a href="https://msdn.microsoft.com/6babdfbd-51d5-4973-9712-f79a95f5f367">IWMRegisteredDevice</a> interface. This interface provides access to information about a registered device in the database that matches the type specified by the <i>dwRegisterType</i> parameter used in the call to <a href="https://msdn.microsoft.com/a11249f5-0604-4de7-9dd2-152d570183c3">GetFirstRegisteredDevice</a>. The information applies to the next device in the list (after the device retrieved previously).


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
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
There are no more devices of the specified type in the list. When this value is returned, the address pointed to by <i>ppDevice</i> is set to <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>ppDevice</i> parameter is <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



To enumerate registered devices of a given type, begin by calling <a href="https://msdn.microsoft.com/a11249f5-0604-4de7-9dd2-152d570183c3">GetFirstRegisteredDevice</a> to retrieve the first device. Then make repeated calls to this method to get subsequent devices from the list. After all devices of the specified types have been retrieved, the next call to <b>GetNextRegisteredDevice</b> returns S_FALSE and the address pointed to by <i>ppDevice</i> is set to <b>NULL</b>.




## -see-also




<a href="https://msdn.microsoft.com/fb08ddae-2abf-4a86-a5d8-ea745ae35aa8">IWMDeviceRegistration Interface</a>
 

 

