---
UID: NF:wmsdkidl.WMCreateDeviceRegistration
title: WMCreateDeviceRegistration function (wmsdkidl.h)
description: The WMCreateDeviceRegistration function creates a device registration object.helpviewer_keywords: ["WMCreateDeviceRegistration","WMCreateDeviceRegistration function [windows Media Format]","wmformat.wmcreatedeviceregistration","wmsdkidl/WMCreateDeviceRegistration"]
old-location: wmformat\wmcreatedeviceregistration.htm
tech.root: wmformat
ms.assetid: 0e318691-07dc-421b-951d-9e65e9160bb0
ms.date: 12/05/2018
ms.keywords: WMCreateDeviceRegistration, WMCreateDeviceRegistration function [windows Media Format], wmformat.wmcreatedeviceregistration, wmsdkidl/WMCreateDeviceRegistration
f1_keywords:
- wmsdkidl/WMCreateDeviceRegistration
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# WMCreateDeviceRegistration function


## -description



The <b>WMCreateDeviceRegistration</b> function creates a device registration object.




## -parameters




### -param ppDevReg [out]

Address of a pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdeviceregistration">IWMDeviceRegistration</a> interface of the newly created device registration object.


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




<a href="https://docs.microsoft.com/windows/desktop/wmformat/functions">Functions</a>
 

 

