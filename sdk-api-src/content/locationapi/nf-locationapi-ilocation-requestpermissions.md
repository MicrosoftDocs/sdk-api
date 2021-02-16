---
UID: NF:locationapi.ILocation.RequestPermissions
title: ILocation::RequestPermissions (locationapi.h)
description: Opens a system dialog box to request user permission to enable location devices.
helpviewer_keywords: ["ILocation interface [WinLocation]","RequestPermissions method","ILocation.RequestPermissions","ILocation::RequestPermissions","RequestPermissions","RequestPermissions method [WinLocation]","RequestPermissions method [WinLocation]","ILocation interface","WinLocation_COM_Ref.ilocation_requestpermissions","locationapi/ILocation::RequestPermissions"]
old-location: winlocation_com_ref\ilocation_requestpermissions.htm
tech.root: winlocation
ms.assetid: eef60203-8705-4f68-be30-c9e7938e5596
ms.date: 12/05/2018
ms.keywords: ILocation interface [WinLocation],RequestPermissions method, ILocation.RequestPermissions, ILocation::RequestPermissions, RequestPermissions, RequestPermissions method [WinLocation], RequestPermissions method [WinLocation],ILocation interface, WinLocation_COM_Ref.ilocation_requestpermissions, locationapi/ILocation::RequestPermissions
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
 - ILocation::RequestPermissions
 - locationapi/ILocation::RequestPermissions
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
 - ILocation.RequestPermissions
---

# ILocation::RequestPermissions


## -description

<p class="CCE_Message">[The Win32 Location API is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use the <a href="/uwp/api/windows.devices.geolocation">Windows.Devices.Geolocation</a>
API.
]

Opens a system dialog box to request user permission to enable location  devices.

## -parameters

### -param hParent [in]

<b>HWND</b> for the parent window. This parameter is optional. In Windows 8 the dialog is always modal if <i>hParent</i> is provided, and not modal if <i>hParent</i> is NULL.

### -param pReportTypes [in]

Pointer to an <b>IID</b> array. This array must contain interface IDs for all report types for which you are requesting permission. The interface IDs of the valid report types are IID_ILatLongReport and  IID_ICivicAddressReport. The count of IDs must match the value specified through the <i>count</i> parameter.

### -param count [in]

The count of interface IDs contained in <i>pReportTypes</i>.

### -param fModal

This parameter is not used.

## -returns

This method can return one of these values.


The following table describes return codes when the call is synchronous.



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
The user enabled location services. The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_ACCESS_DENIED)</b></dt>
</dl>
</td>
<td width="60%">
The location platform is disabled. An administrator turned the location platform off.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_CANCELLED)</b></dt>
</dl>
</td>
<td width="60%">
The user did not enable access to location services or canceled the dialog box.

</td>
</tr>
</table>
 


The following table describes return codes when the call is asynchronous.



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
The user enabled access to location services. The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
An argument is  not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_ACCESS_DENIED) </b></dt>
</dl>
</td>
<td width="60%">
The location platform is disabled. An administrator turned the location platform off. The dialog box was not shown.

</td>
</tr>
</table>

## -remarks

If the user chooses not to enable location services, Windows will not show the  permissions dialog box again.

<div class="alert"><b>Note</b>  Repeated asynchronous calls to <b>RequestPermissions</b> will display multiple instances of the <b>Enable location services</b> dialog box and can potentially flood the screen with dialog boxes, resulting in a poor user experience. If you think that other location sensors might be installed after your first call to <b>RequestPermissions</b>, requiring another call to <b>RequestPermissions</b>, you should either call <b>RequestPermissions</b> synchronously or wait until all location sensors are installed to make an asynchronous call. </div>
<div> </div>
<div class="alert"><b>Note</b>  Making a synchronous call from the user interface (UI) thread of a Windows application can block the UI thread and make the application less responsive. To prevent this, do not make a synchronous call to <b>RequestPermissions</b> from the UI thread.</div>
<div> </div>
<div class="alert"><b>Note</b>  If an  application running in protected mode, such as a Browser Helper Object (BHO) for Internet Explorer, calls <b>RequestPermissions</b>, and the user chooses not to enable location using the dialog box, the location provider will not be enabled, but Windows will display the dialog box again if <b>RequestPermissions</b> is called again by the same user.   </div>
<div> </div>

#### Examples

The following example demonstrates how to call <b>RequestPermissions</b> to request permission for latitude/longitude reports.


```cpp
             // Array of report types of interest. Other ones include IID_ICivicAddressReport
            IID REPORT_TYPES[] = { IID_ILatLongReport };

            // Request permissions for this user account to receive location data for all the
            // types defined in REPORT_TYPES (which is currently just one report type)
            // The last parameter is not used.
            if (FAILED(spLocation->RequestPermissions(
                  NULL, 
                  REPORT_TYPES, 
                  ARRAYSIZE(REPORT_TYPES), 
                  TRUE))) 
            {
                wprintf(L"Warning: Unable to request permissions.\n");
            }


```