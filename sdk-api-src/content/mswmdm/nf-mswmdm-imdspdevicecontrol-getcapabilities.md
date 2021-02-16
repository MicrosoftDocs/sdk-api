---
UID: NF:mswmdm.IMDSPDeviceControl.GetCapabilities
title: IMDSPDeviceControl::GetCapabilities (mswmdm.h)
description: The GetCapabilities method retrieves the capabilities mask for the device with which this control interface is associated. The capabilities describe the methods of the device control that are supported by the media device.
helpviewer_keywords: ["GetCapabilities","GetCapabilities method [windows Media Device Manager]","GetCapabilities method [windows Media Device Manager]","IMDSPDeviceControl interface","IMDSPDeviceControl interface [windows Media Device Manager]","GetCapabilities method","IMDSPDeviceControl.GetCapabilities","IMDSPDeviceControl::GetCapabilities","IMDSPDeviceControlGetCapabilities","mswmdm/IMDSPDeviceControl::GetCapabilities","wmdm.imdspdevicecontrol_getcapabilities"]
old-location: wmdm\imdspdevicecontrol_getcapabilities.htm
tech.root: WMDM
ms.assetid: 5d4e433a-fb2a-43c4-ab7f-fb7168636455
ms.date: 12/05/2018
ms.keywords: GetCapabilities, GetCapabilities method [windows Media Device Manager], GetCapabilities method [windows Media Device Manager],IMDSPDeviceControl interface, IMDSPDeviceControl interface [windows Media Device Manager],GetCapabilities method, IMDSPDeviceControl.GetCapabilities, IMDSPDeviceControl::GetCapabilities, IMDSPDeviceControlGetCapabilities, mswmdm/IMDSPDeviceControl::GetCapabilities, wmdm.imdspdevicecontrol_getcapabilities
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
 - IMDSPDeviceControl::GetCapabilities
 - mswmdm/IMDSPDeviceControl::GetCapabilities
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
 - IMDSPDeviceControl.GetCapabilities
---

# IMDSPDeviceControl::GetCapabilities


## -description

The <b>GetCapabilities</b> method retrieves the capabilities mask for the device with which this control interface is associated. The capabilities describe the methods of the device control that are supported by the media device.

## -parameters

### -param pdwCapabilitiesMask [out]

Pointer to a <b>DWORD</b> containing the capabilities of the device. The following flags can be returned in this variable.

<table>
<tr>
<th>Flag
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>MDM_DEVICECAP_CANPLAY</td>
<td>The media device can play MP3 audio.</td>
</tr>
<tr>
<td>MDM_DEVICECAP_CANSTREAMPLAY</td>
<td>The media device can play streaming audio directly from the host computer.</td>
</tr>
<tr>
<td>MDM_DEVICECAP_CANRECORD</td>
<td>The media device can record audio.</td>
</tr>
<tr>
<td>MDM_DEVICECAP_CANSTREAMRECORD</td>
<td>The media device can record streaming audio directly to the host computer.</td>
</tr>
<tr>
<td>MDM_DEVICECAP_CANPAUSE</td>
<td>The media device can pause during play or record operations.</td>
</tr>
<tr>
<td>MDM_DEVICECAP_CANRESUME</td>
<td>The media device can resume an operation from a pause command.</td>
</tr>
<tr>
<td>MDM_DEVICECAP_CANSTOP</td>
<td>The media device can stop playing before the end of a file.</td>
</tr>
<tr>
<td>MDM_DEVICECAP_CANSEEK</td>
<td>The media device can seek to a position other than the beginning of a file.</td>
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
The <i>pdwCapabilitiesMask</i> parameter is an invalid or <b>NULL</b> pointer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
An unspecified error occurred.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/mswmdm/nn-mswmdm-imdspdevicecontrol">IMDSPDeviceControl Interface</a>