---
UID: NF:mswmdm.IWMDMDevice.GetType
title: IWMDMDevice::GetType (mswmdm.h)
description: The GetType method retrieves the operations supported by the device.
helpviewer_keywords: ["GetType","GetType method [windows Media Device Manager]","GetType method [windows Media Device Manager]","IWMDMDevice interface","IWMDMDevice interface [windows Media Device Manager]","GetType method","IWMDMDevice.GetType","IWMDMDevice::GetType","IWMDMDeviceGetType","mswmdm/IWMDMDevice::GetType","wmdm.iwmdmdevice_gettype"]
old-location: wmdm\iwmdmdevice_gettype.htm
tech.root: WMDM
ms.assetid: b240d6ac-99bd-4cc2-92d8-e9c7c5834bd7
ms.date: 12/05/2018
ms.keywords: GetType, GetType method [windows Media Device Manager], GetType method [windows Media Device Manager],IWMDMDevice interface, IWMDMDevice interface [windows Media Device Manager],GetType method, IWMDMDevice.GetType, IWMDMDevice::GetType, IWMDMDeviceGetType, mswmdm/IWMDMDevice::GetType, wmdm.iwmdmdevice_gettype
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
 - IWMDMDevice::GetType
 - mswmdm/IWMDMDevice::GetType
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
 - IWMDMDevice.GetType
---

# IWMDMDevice::GetType


## -description

The <b>GetType</b> method retrieves the operations supported by the device.

## -parameters

### -param pdwType [out]

Pointer to a <b>DWORD</b> specifying the device type attributes. The possible values returned in <i>pdwType</i> are defined in the following table. Microsoft recommends setting both WMDM_DEVICE_TYPE_SDMI and WMDM_DEVICE_TYPE_NONSDMI flags.

<table>
<tr>
<th>Device type
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>WMDM_DEVICE_TYPE_PLAYBACK</td>
<td>The media device supports audio playback.</td>
</tr>
<tr>
<td>WMDM_DEVICE_TYPE_RECORD</td>
<td>The media device supports audio recording.</td>
</tr>
<tr>
<td>WMDM_DEVICE_TYPE_DECODE</td>
<td>The media device supports audio format decoding.</td>
</tr>
<tr>
<td>WMDM_DEVICE_TYPE_ENCODE</td>
<td>The media device supports audio format encoding.</td>
</tr>
<tr>
<td>WMDM_DEVICE_TYPE_STORAGE</td>
<td>The media device has on-board storage for media files.</td>
</tr>
<tr>
<td>WMDM_DEVICE_TYPE_VIRTUAL</td>
<td>The media device is not a physical device.</td>
</tr>
<tr>
<td>WMDM_DEVICE_TYPE_SDMI</td>
<td>The media device can accept SDMI-protected content.</td>
</tr>
<tr>
<td>WMDM_DEVICE_TYPE_NONSDMI</td>
<td>The media device can accept non-SDMI content.</td>
</tr>
<tr>
<td>WMDM_DEVICE_TYPE_NONREENTRANT</td>
<td>The media device must synchronize access to Windows Media Device Manager services.</td>
</tr>
<tr>
<td>WMDM_DEVICE_TYPE_FILELISTRESYNC</td>
<td>The media device allows the file list to be resynchronized.</td>
</tr>
<tr>
<td>WMDM_DEVICE_TYPE_VIEW_PREF_METADATAVIEW</td>
<td>The media device prefers metadata views while its storages are enumerated.</td>
</tr>
</table>

## -returns

The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="/windows/desktop/WMDM/error-codes">Error Codes</a>.

## -remarks

The current Microsoft service providers may not provide reliable information about devices, except WMDM_DEVICE_TYPE_NONSDMI or WMDM_DEVICE_TYPE_SDMI. All devices will be reported as supporting the former; devices that support serial numbers also return the latter.

## -see-also

<a href="/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice">IWMDMDevice Interface</a>



<a href="/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice-getname">IWMDMDevice::GetName</a>