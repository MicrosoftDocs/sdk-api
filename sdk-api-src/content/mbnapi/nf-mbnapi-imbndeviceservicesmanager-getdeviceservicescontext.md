---
UID: NF:mbnapi.IMbnDeviceServicesManager.GetDeviceServicesContext
title: IMbnDeviceServicesManager::GetDeviceServicesContext
author: windows-sdk-content
description: Gets the IMbnDeviceServicesContext interface for a specific Mobile Broadband device.
old-location: mbn\imbndeviceservicesmanager_getdeviceservicescontext.htm
old-project: mbn
ms.assetid: 20AD207B-6FC3-4493-81F7-41619CA703DB
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: GetDeviceServicesContext, GetDeviceServicesContext method [Microsoft Broadband Networks], GetDeviceServicesContext method [Microsoft Broadband Networks],IMbnDeviceServicesManager interface, IMbnDeviceServicesManager interface [Microsoft Broadband Networks],GetDeviceServicesContext method, IMbnDeviceServicesManager.GetDeviceServicesContext, IMbnDeviceServicesManager::GetDeviceServicesContext, mbn.imbndeviceservicesmanager_getdeviceservicescontext, mbnapi/IMbnDeviceServicesManager::GetDeviceServicesContext
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mbnapi.h
req.include-header: 
req.redist: 
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
 - IMbnDeviceServicesManager.GetDeviceServicesContext
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMbnDeviceServicesManager::GetDeviceServicesContext


## -description


Gets the <a href="https://msdn.microsoft.com/0B97FCCD-0A90-4FA2-9122-B00BD3F1A033">IMbnDeviceServicesContext</a> interface for a specific Mobile Broadband device


## -parameters




### -param networkInterfaceID [in]

A string that contains the ID of the Mobile Broadband device. The ID can be obtained using the <a href="https://msdn.microsoft.com/9828567b-ef5e-44b7-90ce-1788cd8dd947">InterfaceID</a> property


### -param mbnDevicesContext [out, retval]

Pointer to the address of the <a href="https://msdn.microsoft.com/0B97FCCD-0A90-4FA2-9122-B00BD3F1A033">IMbnDeviceServicesContext</a> for the device specified by <i>networkInterfaceID</i> or <b>NULL</b> if there is no matching interface.


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
<dt><b>HRESULT_FROM_WIN32(ERROR_NOT_FOUND)</b></dt>
</dl>
</td>
<td width="60%">
There is no available device matching the specified interface ID.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>mbnDeviceServicesContext</i> parameter is NULL.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Could not allocate the required memory.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/6CFF2275-0649-4009-84F2-0657B2FF281C">IMbnDeviceServicesManager</a>
 

 

