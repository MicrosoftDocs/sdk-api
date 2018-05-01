---
UID: NF:wmsdkidl.IWMRegisteredDevice.SetAttributeByName
title: IWMRegisteredDevice::SetAttributeByName method
author: windows-driver-content
description: The SetAttributeByName method sets a device attribute.
old-location: wmformat\iwmregistereddevice_setattributebyname.htm
old-project: wmformat
ms.assetid: 49562f2a-1bb5-46d7-81cc-c13b66cf691f
ms.author: windowsdriverdev
ms.date: 4/13/2018
ms.keywords: IWMRegisteredDevice, IWMRegisteredDevice interface [windows Media Format], SetAttributeByName method, IWMRegisteredDevice::SetAttributeByName, IWMRegisteredDeviceSetAttributeByName, SetAttributeByName method [windows Media Format], SetAttributeByName method [windows Media Format], IWMRegisteredDevice interface, SetAttributeByName,IWMRegisteredDevice.SetAttributeByName, wmformat.iwmregistereddevice_setattributebyname, wmsdkidl/IWMRegisteredDevice::SetAttributeByName
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
-	IWMRegisteredDevice.SetAttributeByName
product: Windows
targetos: Windows
req.lib: WMStubDRM.lib
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMRegisteredDevice::SetAttributeByName method


## -description



The <b>SetAttributeByName</b> method sets a device attribute.




## -parameters




### -param bstrName [in]

Name of the attribute to set.


### -param bstrValue [in]

Value of the attribute.


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



<a href="https://msdn.microsoft.com/e74bd544-295d-4e83-8804-5a99d7efdbb8">IWMRegisteredDevice::GetAttributeByName</a>
 

 

