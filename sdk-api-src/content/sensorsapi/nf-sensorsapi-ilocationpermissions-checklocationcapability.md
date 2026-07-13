---
UID: NF:sensorsapi.ILocationPermissions.CheckLocationCapability
title: ILocationPermissions::CheckLocationCapability (sensorsapi.h)
description: Gets the location capability of the Windows Store app of the given thread.
helpviewer_keywords: ["CheckLocationCapability","CheckLocationCapability method","CheckLocationCapability method","ILocationPermissions interface","ILocationPermissions interface","CheckLocationCapability method","ILocationPermissions.CheckLocationCapability","ILocationPermissions::CheckLocationCapability","sensorsapi/ILocationPermissions::CheckLocationCapability","winsensors.ilocationpermissions_checklocationcapability"]
old-location: winsensors\ilocationpermissions_checklocationcapability.htm
tech.root: winsensors
ms.assetid: B7D6268C-4A0D-490F-B1E7-573159EF7CFF
ms.date: 09/19/2025
ms.keywords: CheckLocationCapability, CheckLocationCapability method, CheckLocationCapability method,ILocationPermissions interface, ILocationPermissions interface,CheckLocationCapability method, ILocationPermissions.CheckLocationCapability, ILocationPermissions::CheckLocationCapability, sensorsapi/ILocationPermissions::CheckLocationCapability, winsensors.ilocationpermissions_checklocationcapability
req.header: sensorsapi.h
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
 - ILocationPermissions::CheckLocationCapability
 - sensorsapi/ILocationPermissions::CheckLocationCapability
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - sensorsapi.h
api_name:
 - ILocationPermissions.CheckLocationCapability
---

# ILocationPermissions::CheckLocationCapability


## -description

> [!IMPORTANT]
> Use the [UWP Sensor API](/windows/uwp/devices-sensors/sensors) instead.
>
> The COM-based Sensor API is deprecated and should not be used in new applications. No additional features or enhancements are planned, and support will be limited.

Gets the location capability of the Windows Store app of the given thread

## -parameters

### -param dwClientThreadId

Thread Id of the app to check the location capability of

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
The method succeeded and the app is location enabled.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ACCESSDENIED</b></dt>
</dl>
</td>
<td width="60%">
The app has not declared location capability or the user has declined or revoked location access.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ILLEGAL_METHOD_CALL</b></dt>
</dl>
</td>
<td width="60%">
An invalid client thread was provided.

</td>
</tr>
</table>

## -remarks

<div class="alert"><b>Note</b>  <b>CheckLocationCapability</b> is available in Windows 8.</div>
<div> </div>
For more information on location settings in Windows 8 see <a href="/previous-versions/windows">Location settings</a>.

## -see-also

<a href="/windows/desktop/api/sensorsapi/nn-sensorsapi-ilocationpermissions">ILocationPermissions</a>