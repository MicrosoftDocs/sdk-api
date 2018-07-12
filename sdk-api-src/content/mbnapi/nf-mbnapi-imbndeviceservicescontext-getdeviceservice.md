---
UID: NF:mbnapi.IMbnDeviceServicesContext.GetDeviceService
title: IMbnDeviceServicesContext::GetDeviceService
author: windows-sdk-content
description: Gets the IMbnDeviceService object that can be used for communicating with a device service on the Mobile Broadband device.
old-location: mbn\imbndeviceservicescontext_getdeviceservice.htm
old-project: mbn
ms.assetid: 293E9BE5-AD7D-41B7-9A27-E964EE745183
ms.author: windowssdkdev
ms.date: 06/05/2018
ms.keywords: GetDeviceService, GetDeviceService method [Microsoft Broadband Networks], GetDeviceService method [Microsoft Broadband Networks],IMbnDeviceServicesContext interface, IMbnDeviceServicesContext interface [Microsoft Broadband Networks],GetDeviceService method, IMbnDeviceServicesContext.GetDeviceService, IMbnDeviceServicesContext::GetDeviceService, mbn.imbndeviceservicescontext_getdeviceservice, mbnapi/IMbnDeviceServicesContext::GetDeviceService
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mbnapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps | UWP apps]
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
 - IMbnDeviceServicesContext.GetDeviceService
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMbnDeviceServicesContext::GetDeviceService


## -description


Gets the <a href="https://msdn.microsoft.com/library/Hh780509(v=VS.85).aspx">IMbnDeviceService</a> object that can be used for communicating with a device service on the Mobile Broadband device.


## -parameters




### -param deviceServiceID [in]

The <a href="https://msdn.microsoft.com/3AE6D7A6-3974-4517-AEB6-992CAC543247">deviceServiceID</a> of the Mobile Broadband device.


### -param mbnDeviceService [out, retval]

The <a href="https://msdn.microsoft.com/library/Hh780509(v=VS.85).aspx">IMbnDeviceService</a> object.


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
<dt><b>Other</b></dt>
</dl>
</td>
<td width="60%">
An error was encountered when executing this method.

</td>
</tr>
</table>
 




## -remarks



<b>GetDeviceService</b> may return an <a href="https://msdn.microsoft.com/library/Hh780509(v=VS.85).aspx">IMbnDeviceService</a> object that already has a command or data session open. The calling process can check if the device service is already open.




## -see-also




<a href="https://msdn.microsoft.com/0B97FCCD-0A90-4FA2-9122-B00BD3F1A033">IMbnDeviceServicesContext</a>
 

 

