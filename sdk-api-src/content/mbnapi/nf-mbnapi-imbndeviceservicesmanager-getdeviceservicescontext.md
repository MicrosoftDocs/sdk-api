---
UID: NF:mbnapi.IMbnDeviceServicesManager.GetDeviceServicesContext
title: IMbnDeviceServicesManager::GetDeviceServicesContext (mbnapi.h)
description: Gets the IMbnDeviceServicesContext interface for a specific Mobile Broadband device.
helpviewer_keywords: ["GetDeviceServicesContext","GetDeviceServicesContext method [Microsoft Broadband Networks]","GetDeviceServicesContext method [Microsoft Broadband Networks]","IMbnDeviceServicesManager interface","IMbnDeviceServicesManager interface [Microsoft Broadband Networks]","GetDeviceServicesContext method","IMbnDeviceServicesManager.GetDeviceServicesContext","IMbnDeviceServicesManager::GetDeviceServicesContext","mbn.imbndeviceservicesmanager_getdeviceservicescontext","mbnapi/IMbnDeviceServicesManager::GetDeviceServicesContext"]
old-location: mbn\imbndeviceservicesmanager_getdeviceservicescontext.htm
tech.root: mbn
ms.assetid: 20AD207B-6FC3-4493-81F7-41619CA703DB
ms.date: 12/05/2018
ms.keywords: GetDeviceServicesContext, GetDeviceServicesContext method [Microsoft Broadband Networks], GetDeviceServicesContext method [Microsoft Broadband Networks],IMbnDeviceServicesManager interface, IMbnDeviceServicesManager interface [Microsoft Broadband Networks],GetDeviceServicesContext method, IMbnDeviceServicesManager.GetDeviceServicesContext, IMbnDeviceServicesManager::GetDeviceServicesContext, mbn.imbndeviceservicesmanager_getdeviceservicescontext, mbnapi/IMbnDeviceServicesManager::GetDeviceServicesContext
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMbnDeviceServicesManager::GetDeviceServicesContext
 - mbnapi/IMbnDeviceServicesManager::GetDeviceServicesContext
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mbnapi.h
api_name:
 - IMbnDeviceServicesManager.GetDeviceServicesContext
---

# IMbnDeviceServicesManager::GetDeviceServicesContext


## -description

> [!IMPORTANT]
> Starting in Windows 10, version 1803, the Win32 APIs described in this section are replaced by the Windows Runtime APIs in the [Windows.Networking.Connectivity](/uwp/api/windows.networking.connectivity) namespace.

Gets the <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbndeviceservicescontext">IMbnDeviceServicesContext</a> interface for a specific Mobile Broadband device

## -parameters

### -param networkInterfaceID [in]

A string that contains the ID of the Mobile Broadband device. The ID can be obtained using the <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbninterface-get_interfaceid">InterfaceID</a> property

### -param mbnDevicesContext [out, retval]

Pointer to the address of the <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbndeviceservicescontext">IMbnDeviceServicesContext</a> for the device specified by <i>networkInterfaceID</i> or <b>NULL</b> if there is no matching interface.

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

<a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbndeviceservicesmanager">IMbnDeviceServicesManager</a>