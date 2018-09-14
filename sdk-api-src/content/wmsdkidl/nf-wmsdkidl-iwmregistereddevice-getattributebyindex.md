---
UID: NF:wmsdkidl.IWMRegisteredDevice.GetAttributeByIndex
title: IWMRegisteredDevice::GetAttributeByIndex
author: windows-sdk-content
description: The GetAttributeByIndex method retrieves an attribute associated with the device. This method uses the attribute index to specify the attribute to retrieve.
old-location: wmformat\iwmregistereddevice_getattributebyindex.htm
tech.root: wmformat
ms.assetid: 02a582d4-329e-47e3-9dbe-dba8a3e4b4b3
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: GetAttributeByIndex, GetAttributeByIndex method [windows Media Format], GetAttributeByIndex method [windows Media Format],IWMRegisteredDevice interface, IWMRegisteredDevice interface [windows Media Format],GetAttributeByIndex method, IWMRegisteredDevice.GetAttributeByIndex, IWMRegisteredDevice::GetAttributeByIndex, IWMRegisteredDeviceGetAttributeByIndex, wmformat.iwmregistereddevice_getattributebyindex, wmsdkidl/IWMRegisteredDevice::GetAttributeByIndex
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
 - IWMRegisteredDevice.GetAttributeByIndex
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMRegisteredDevice::GetAttributeByIndex


## -description



The <b>GetAttributeByIndex</b> method retrieves an attribute associated with the device. This method uses the attribute index to specify the attribute to retrieve.




## -parameters




### -param dwIndex [in]

Attribute index. Valid indexes range from zero to one less than the number of attributes returned by <a href="https://msdn.microsoft.com/6032cb18-4c4a-4cd7-905e-5cb390bfc37b">GetAttributeCount</a>.


### -param pbstrName [out]

Address of a variable that receives the attribute name.


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
 

 

