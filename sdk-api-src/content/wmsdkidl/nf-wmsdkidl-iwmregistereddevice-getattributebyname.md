---
UID: NF:wmsdkidl.IWMRegisteredDevice.GetAttributeByName
title: IWMRegisteredDevice::GetAttributeByName
author: windows-sdk-content
description: The GetAttributeByName method retrieves an attribute associated with the device. This method uses an attribute name to specify the attribute to retrieve.
old-location: wmformat\iwmregistereddevice_getattributebyname.htm
tech.root: wmformat
ms.assetid: e74bd544-295d-4e83-8804-5a99d7efdbb8
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: GetAttributeByName, GetAttributeByName method [windows Media Format], GetAttributeByName method [windows Media Format],IWMRegisteredDevice interface, IWMRegisteredDevice interface [windows Media Format],GetAttributeByName method, IWMRegisteredDevice.GetAttributeByName, IWMRegisteredDevice::GetAttributeByName, IWMRegisteredDeviceGetAttributeByName, wmformat.iwmregistereddevice_getattributebyname, wmsdkidl/IWMRegisteredDevice::GetAttributeByName
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IWMRegisteredDevice.GetAttributeByName
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMRegisteredDevice::GetAttributeByName


## -description



The <b>GetAttributeByName</b> method retrieves an attribute associated with the device. This method uses an attribute name to specify the attribute to retrieve.




## -parameters




### -param bstrName [in]

Name of the attribute to retrieve.


### -param pbstrValue [out]

Address of a variable that receives the attribute value.


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




<a href="https://msdn.microsoft.com/6babdfbd-51d5-4973-9712-f79a95f5f367">IWMRegisteredDevice Interface</a>



<a href="https://msdn.microsoft.com/49562f2a-1bb5-46d7-81cc-c13b66cf691f">IWMRegisteredDevice::SetAttributeByName</a>
 

 

