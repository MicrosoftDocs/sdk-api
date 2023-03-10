---
UID: NF:locationapi.IDefaultLocation.SetReport
title: IDefaultLocation::SetReport (locationapi.h)
description: Sets the default location.
helpviewer_keywords: ["IDefaultLocation interface [WinLocation]","SetReport method","IDefaultLocation.SetReport","IDefaultLocation::SetReport","SetReport","SetReport method [WinLocation]","SetReport method [WinLocation]","IDefaultLocation interface","WinLocation_COM_Ref.idefaultlocation_setreport","locationapi/IDefaultLocation::SetReport"]
old-location: winlocation_com_ref\idefaultlocation_setreport.htm
tech.root: winlocation
ms.assetid: 50355f93-e609-44d5-925a-2de7af1e0564
ms.date: 12/05/2018
ms.keywords: IDefaultLocation interface [WinLocation],SetReport method, IDefaultLocation.SetReport, IDefaultLocation::SetReport, SetReport, SetReport method [WinLocation], SetReport method [WinLocation],IDefaultLocation interface, WinLocation_COM_Ref.idefaultlocation_setreport, locationapi/IDefaultLocation::SetReport
req.header: locationapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only],Windows 7
req.target-min-winversvr: None supported
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
req.dll: LocationAPI.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDefaultLocation::SetReport
 - locationapi/IDefaultLocation::SetReport
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - LocationAPI.dll
api_name:
 - IDefaultLocation.SetReport
---

# IDefaultLocation::SetReport


## -description

<p class="CCE_Message">[The Win32 Location API is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use the <a href="/uwp/api/windows.devices.geolocation">Windows.Devices.Geolocation</a> API.
]

Sets the default location.

## -parameters

### -param reportType [in]

<b>REFIID</b> that represents the interface ID of the type of report that is passed using <i>pLocationReport</i>.

### -param pLocationReport [in]

Pointer to the <a href="/windows/desktop/api/locationapi/nn-locationapi-ilocationreport">ILocationReport</a> instance that contains the location report from the default location provider.

## -returns

Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>S_OK</dt>
</dl>
</td>
<td width="60%">
The location report was successfully set.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>E_INVALIDARG</dt>
</dl>
</td>
<td width="60%">
The location report contains invalid data.  This may occur when a civic address report does not contain a valid IS0 3166 two-letter country or region code, or when a latitude/longitude report does not contain a latitude between -90 and 90 or does not contain a longitude between -180 and 180. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>E_ACCESSDENIED</dt>
</dl>
</td>
<td width="60%">
The user does not have permission to set the default location.

</td>
</tr>
</table>

## -remarks

<a href="/windows/desktop/api/locationapi/nn-locationapi-ilocationreport">ILocationReport</a> is the base interface of specific location report types. The actual interface you use for <i>pLocationReport</i> must match the type you specify through <i>reportType</i>.

Note that the type specified by <i>reportType</i> must be the <b>IID</b> of either <a href="/windows/desktop/api/locationapi/nn-locationapi-icivicaddressreport">ICivicAddressReport</a> or <a href="/windows/desktop/api/locationapi/nn-locationapi-ilatlongreport">ILatLongReport</a>.

The latitude and longitude provided in a latitude/longitude report must correspond to a location on the globe. Otherwise this method returns an <b>HRESULT</b> error value.

<div class="alert"><b>Note</b>  An application does not receive the expected location change event from <a href="/windows/desktop/api/locationapi/nf-locationapi-ilocationevents-onlocationchanged">OnLocationChanged</a> if both of the following conditions are true. First, the application runs as a service, in the context of the LOCALSERVICE, SYSTEM, or NETWORKSERVICE user account. Second, the location change event results from changing the default location, either manually when the user selects <b>Default Location</b> in Control Panel, or programmatically when an application calls <a href="/windows/desktop/api/locationapi/nn-locationapi-idefaultlocation">IDefaultLocation::SetReport</a>.</div>
<div> </div>

#### Examples

The following example shows how to set the default location using a civic address report.


```cpp
            // set the civic address fields of the Default Location
            hr = spDefaultLocation->SetReport(IID_ICivicAddressReport, spCivicAddressReport);
            if (E_INVALIDARG == hr)
            {
                wprintf(L"The civic address report has invalid data. ");
                wprintf(L"Country/region must be a valid ISO-3166 2-letter or 3-letter code.\n");
            }
            else if (E_ACCESSDENIED == hr)
            {
                wprintf(L"Administrator privilege required.\n");
            }

```

## -see-also

<a href="/windows/desktop/api/locationapi/nn-locationapi-idefaultlocation">IDefaultLocation</a>