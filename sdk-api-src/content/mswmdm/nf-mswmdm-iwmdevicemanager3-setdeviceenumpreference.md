---
UID: NF:mswmdm.IWMDeviceManager3.SetDeviceEnumPreference
title: IWMDeviceManager3::SetDeviceEnumPreference (mswmdm.h)
description: The SetDeviceEnumPreference method sets the device enumeration preferences. (IWMDeviceManager3.SetDeviceEnumPreference)
helpviewer_keywords: ["IWMDeviceManager3 interface [windows Media Device Manager]","SetDeviceEnumPreference method","IWMDeviceManager3.SetDeviceEnumPreference","IWMDeviceManager3::SetDeviceEnumPreference","IWMDeviceManager3SetDeviceEnumPreference","SetDeviceEnumPreference","SetDeviceEnumPreference method [windows Media Device Manager]","SetDeviceEnumPreference method [windows Media Device Manager]","IWMDeviceManager3 interface","mswmdm/IWMDeviceManager3::SetDeviceEnumPreference","wmdm.iwmdevicemanager3_setdeviceenumpreference"]
old-location: wmdm\iwmdevicemanager3_setdeviceenumpreference.htm
tech.root: WMDM
ms.assetid: a39aaa62-6f23-4fe0-9231-1781ce74b090
ms.date: 12/05/2018
ms.keywords: IWMDeviceManager3 interface [windows Media Device Manager],SetDeviceEnumPreference method, IWMDeviceManager3.SetDeviceEnumPreference, IWMDeviceManager3::SetDeviceEnumPreference, IWMDeviceManager3SetDeviceEnumPreference, SetDeviceEnumPreference, SetDeviceEnumPreference method [windows Media Device Manager], SetDeviceEnumPreference method [windows Media Device Manager],IWMDeviceManager3 interface, mswmdm/IWMDeviceManager3::SetDeviceEnumPreference, wmdm.iwmdevicemanager3_setdeviceenumpreference
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWMDeviceManager3::SetDeviceEnumPreference
 - mswmdm/IWMDeviceManager3::SetDeviceEnumPreference
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mswmdm.h
api_name:
 - IWMDeviceManager3.SetDeviceEnumPreference
---

# IWMDeviceManager3::SetDeviceEnumPreference


## -description

The <b>SetDeviceEnumPreference</b> method sets the device enumeration preferences.

## -parameters

### -param dwEnumPref [in]

Specifies a bitwise <b>OR</b> combination of one or more of the following bit values that specify enumeration preference. Each set bit enables the corresponding extended behavior, whereas the absence of that bit disables the extended behavior and specifies the default, backward-compatible enumeration behavior. The possible values for <i>fuPrefs</i> are provided in the following table.

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>DO_NOT_VIRTUALIZE_STORAGES_AS_DEVICES</td>
<td>By default, for devices containing multiple storage media (for example, multiple flash memory cards), each of these storages enumerates as a separate pseudo-device. However, when this flag is set, storages are not visible as devices, and only devices are visible as devices. See Remarks for more information.</td>
</tr>
<tr>
<td>ALLOW_OUTOFBAND_NOTIFICATION</td>
<td>When this flag is set, the service provider can send device arrival and removal by an additional mechanism, such as by using a window message, as well as the default mechanism of calling any application-implemented <a href="/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmnotification">IWMDMNotification</a> interfaces.</td>
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
The <i>fuPrefs</i> parameter specifies an unsupported bit value.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WMDM_E_CALL_OUT_OF_SEQUENCE</b></dt>
</dl>
</td>
<td width="60%">
The method was called after an enumeration operation; it must be called before the enumeration operation.

</td>
</tr>
</table>

## -remarks

This method provides clients the ability to override the default device enumeration behavior of Windows Media Device Manager. In order to override the default behavior, the client application must call this method immediately after creating the device manager object by querying for the <b>IWMDMDeviceManager3</b>  interface from Media Device Manager. The call must be made before any enumeration occurs, either explicitly or implicitly as a result of another operation.

After a preference flag is set, it cannot be changed for the lifetime of the application (not just the lifetime of the Windows Media Device Manager object). Attempting to change a preference flag will result in an error. Calling this method again with the same flag settings does not return an error, and also does have any effect on enumeration.

The service provider may not honor the DO_NOT_VIRTUALIZE_STORAGES_AS_DEVICES flag. A more robust way to determine if storages are hosted by the same device is to call <a href="/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice2-getcanonicalname">IWMDMDevice2::GetCanonicalName</a>. Storages from the same device will return identical values, except for the final digit after the last "$" character.

## -see-also

<a href="/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice2-getcanonicalname">IWMDMDevice2::GetCanonicalName</a>
