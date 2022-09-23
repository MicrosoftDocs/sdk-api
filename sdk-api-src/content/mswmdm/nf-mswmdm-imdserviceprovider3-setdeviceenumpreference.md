---
UID: NF:mswmdm.IMDServiceProvider3.SetDeviceEnumPreference
title: IMDServiceProvider3::SetDeviceEnumPreference (mswmdm.h)
description: The SetDeviceEnumPreference method sets the device enumeration preferences. (IMDServiceProvider3.SetDeviceEnumPreference)
helpviewer_keywords: ["IMDServiceProvider3 interface [windows Media Device Manager]","SetDeviceEnumPreference method","IMDServiceProvider3.SetDeviceEnumPreference","IMDServiceProvider3::SetDeviceEnumPreference","IMDServiceProvider3SetDeviceEnumPreference","SetDeviceEnumPreference","SetDeviceEnumPreference method [windows Media Device Manager]","SetDeviceEnumPreference method [windows Media Device Manager]","IMDServiceProvider3 interface","mswmdm/IMDServiceProvider3::SetDeviceEnumPreference","wmdm.imdserviceprovider3_setdeviceenumpreference"]
old-location: wmdm\imdserviceprovider3_setdeviceenumpreference.htm
tech.root: WMDM
ms.assetid: f3807e80-82ea-437e-ab30-bd00bc0fc6ad
ms.date: 12/05/2018
ms.keywords: IMDServiceProvider3 interface [windows Media Device Manager],SetDeviceEnumPreference method, IMDServiceProvider3.SetDeviceEnumPreference, IMDServiceProvider3::SetDeviceEnumPreference, IMDServiceProvider3SetDeviceEnumPreference, SetDeviceEnumPreference, SetDeviceEnumPreference method [windows Media Device Manager], SetDeviceEnumPreference method [windows Media Device Manager],IMDServiceProvider3 interface, mswmdm/IMDServiceProvider3::SetDeviceEnumPreference, wmdm.imdserviceprovider3_setdeviceenumpreference
req.header: mswmdm.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mssachlp.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMDServiceProvider3::SetDeviceEnumPreference
 - mswmdm/IMDServiceProvider3::SetDeviceEnumPreference
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mssachlp.lib
 - mssachlp.dll
api_name:
 - IMDServiceProvider3.SetDeviceEnumPreference
---

# IMDServiceProvider3::SetDeviceEnumPreference


## -description

The <b>SetDeviceEnumPreference</b> method sets the device enumeration preferences.

## -parameters

### -param dwEnumPref [in]

Contains a bitwise <b>OR</b> combination of one or more of the following bit values that specify enumeration preference. Each set bit enables the corresponding extended behavior, whereas the absence of that bit disables the extended behavior and specifies the default, backward-compatible enumeration behavior. The possible values for <i>dwEnumPref</i> are provided in the following table.

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>DO_NOT_VIRTUALIZE_STORAGES_AS_DEVICES</td>
<td>By default, for devices containing multiple storage media, each of these storages enumerates as a separate pseudo-device. However, when this bit is set, storages are not visible as devices, and only devices are visible as devices.</td>
</tr>
<tr>
<td>ALLOW_OUTOFBAND_NOTIFICATION</td>
<td>By default, the <a href="/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmnotification">IWMDMNotification</a> callback mechanism provides applications with device arrival and removal events. When this bit is set, the service provider is free to notify the application by a separate mechanism, such as by using a window message. This behavior is in addition to the Windows Media Device Manager notifications. This flag does not suppress Windows Media Device Manager notifications.</td>
</tr>
</table>

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
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>dwEnumPref</i> parameter contains an unsupported bit value.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WMDM_E_CALL_OUT_OF_SEQUENCE</b></dt>
</dl>
</td>
<td width="60%">
The method was called after an enumeration operation. It must be called before the enumeration operation.

</td>
</tr>
</table>

## -remarks

This API provides clients the ability to override the default device enumeration behavior of Windows Media Device Manager.

Client applications must call this method immediately after creating the device manager object by querying for the <a href="/windows/desktop/api/mswmdm/nn-mswmdm-iwmdevicemanager">IWMDeviceManager</a> interface from Windows Media Device Manager. The call must be made before any enumeration occurs, either explicitly or implicitly as a result of another operation.

After a preference flag is set, it cannot be changed for the lifetime of the application (not just the lifetime of the Windows Media Device Manager object). Attempting to change a preference flag will result in an error. Calling this API again with the same flag settings does not return an error, and also does have any effect on enumeration.

The DO_NOT_VIRTUALIZE_STORAGES_AS_DEVICES flag has to be honored by the service provider to take effect. It is possible that, despite this flag, some devices are enumerated as a device-per-storage.

## -see-also

<a href="/windows/desktop/api/mswmdm/nn-mswmdm-imdserviceprovider3">IMDServiceProvider3 Interface</a>
