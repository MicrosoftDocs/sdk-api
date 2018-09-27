---
UID: NF:wmsdkidl.WMCreateDeviceRegistration
title: WMCreateDeviceRegistration function
author: windows-sdk-content
description: The WMCreateDeviceRegistration function creates a device registration object.
old-location: wmformat\wmcreatedeviceregistration.htm
tech.root: wmformat
ms.assetid: 0e318691-07dc-421b-951d-9e65e9160bb0
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: WMCreateDeviceRegistration, WMCreateDeviceRegistration function [windows Media Format], wmformat.wmcreatedeviceregistration, wmsdkidl/WMCreateDeviceRegistration
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
req.lib: Wmvcore.lib
req.dll: Wmvcore.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wmvcore.dll
api_name:
 - WMCreateDeviceRegistration
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# WMCreateDeviceRegistration function


## -description



The <b>WMCreateDeviceRegistration</b> function creates a device registration object.




## -parameters




### -param ppDevReg [out]

Address of a pointer to the <a href="https://msdn.microsoft.com/fb08ddae-2abf-4a86-a5d8-ea745ae35aa8">IWMDeviceRegistration</a> interface of the newly created device registration object.


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
The function succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The ppDevReg parameter is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
The function is unable to allocate memory for the new object.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/10fa8f96-8030-4727-af5d-7c06229d05d8">Functions</a>
 

 

