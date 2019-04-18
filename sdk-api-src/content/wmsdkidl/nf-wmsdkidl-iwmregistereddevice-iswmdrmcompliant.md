---
UID: NF:wmsdkidl.IWMRegisteredDevice.IsWmdrmCompliant
title: IWMRegisteredDevice::IsWmdrmCompliant (wmsdkidl.h)
author: windows-sdk-content
description: The IsWmdrmCompliant method retrieves the DRM compliance status of the device. Compliant devices can receive data using the Windows Media DRM 10 for Network Devices protocol.
old-location: wmformat\iwmregistereddevice_iswmdrmcompliant.htm
tech.root: wmformat
ms.assetid: 45bc7abb-1d39-4988-a9f0-867eaefe148f
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWMRegisteredDevice interface [windows Media Format],IsWmdrmCompliant method, IWMRegisteredDevice.IsWmdrmCompliant, IWMRegisteredDevice::IsWmdrmCompliant, IWMRegisteredDeviceIsWmdrmCompliant, IsWmdrmCompliant, IsWmdrmCompliant method [windows Media Format], IsWmdrmCompliant method [windows Media Format],IWMRegisteredDevice interface, wmformat.iwmregistereddevice_iswmdrmcompliant, wmsdkidl/IWMRegisteredDevice::IsWmdrmCompliant
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
req.lib: WMStubDRM.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - WMStubDRM.lib
 - WMStubDRM.dll
api_name:
 - IWMRegisteredDevice.IsWmdrmCompliant
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMRegisteredDevice::IsWmdrmCompliant


## -description



The <b>IsWmdrmCompliant</b> method retrieves the DRM compliance status of the device. Compliant devices can receive data using the Windows Media DRM 10 for Network Devices protocol.




## -parameters




### -param pfCompliant [out]

Address of a variable that receives the device DRM compliance status. <b>TRUE</b> indicates that Windows Media DRM 10 for Network Devices is supported.


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
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd743621(v=VS.85).aspx">IWMRegisteredDevice Interface</a>
 

 

