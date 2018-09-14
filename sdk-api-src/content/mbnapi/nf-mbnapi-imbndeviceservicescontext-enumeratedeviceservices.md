---
UID: NF:mbnapi.IMbnDeviceServicesContext.EnumerateDeviceServices
title: IMbnDeviceServicesContext::EnumerateDeviceServices
author: windows-sdk-content
description: Gets the list of supported device services by the Mobile Broadband device.
old-location: mbn\imbndeviceservicescontext_enumeratedeviceservices.htm
tech.root: mbn
ms.assetid: 90CB9B2E-16CA-48A0-AF16-937D816718D6
ms.author: windowssdkdev
ms.date: 08/31/2018
ms.keywords: EnumerateDeviceServices, EnumerateDeviceServices method [Microsoft Broadband Networks], EnumerateDeviceServices method [Microsoft Broadband Networks],IMbnDeviceServicesContext interface, IMbnDeviceServicesContext interface [Microsoft Broadband Networks],EnumerateDeviceServices method, IMbnDeviceServicesContext.EnumerateDeviceServices, IMbnDeviceServicesContext::EnumerateDeviceServices, mbn.imbndeviceservicescontext_enumeratedeviceservices, mbnapi/IMbnDeviceServicesContext::EnumerateDeviceServices
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mbnapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mbnapi.h
api_name:
 - IMbnDeviceServicesContext.EnumerateDeviceServices
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMbnDeviceServicesContext::EnumerateDeviceServices


## -description


Gets the list of supported device services by the Mobile Broadband device.


## -parameters




### -param deviceServices [out, retval]

Pointer to an array of <a href="https://msdn.microsoft.com/83BB1CC3-2F00-4CB0-AF05-A8309D01942D">MBN_DEVICE_SERVICE</a> structures that contains the list of device service supported by the device. If <b>EnumerateDeviceServices</b> returns any value other than <b>S_OK</b>, <i>deviceServices</i> is <b>NULL</b>. Otherwise, upon completion, the calling program must free the allocated memory. Before freeing the array by calling <a href="https://msdn.microsoft.com/fc94f7e7-b903-4c78-905c-54df1f8d13fa">SafeArrayDestroy</a>, the calling program must also free all the <b>BSTRs</b> in the<b>MBN_DEVICE_SERVICE</b> structure by calling <a href="https://msdn.microsoft.com/8f230ee3-5f6e-4cb9-a910-9c90b754dcd3">SysFreeString</a>.


## -returns



The method can return one of the following values.

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
The method completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_NOT_SUPPORTED)</b></dt>
</dl>
</td>
<td width="60%">
The device does not support any device services.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_PENDING</b></dt>
</dl>
</td>
<td width="60%">
The information is not available. The Mobile Broadband service is currently probing the device to retrieve this information.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>Other</b></dt>
</dl>
</td>
<td width="60%">
An error was encountered when executing this method.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/0B97FCCD-0A90-4FA2-9122-B00BD3F1A033">IMbnDeviceServicesContext</a>
 

 

