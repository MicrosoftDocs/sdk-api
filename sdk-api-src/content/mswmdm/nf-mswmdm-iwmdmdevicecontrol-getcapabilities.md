---
UID: NF:mswmdm.IWMDMDeviceControl.GetCapabilities
title: IWMDMDeviceControl::GetCapabilities (mswmdm.h)
description: The GetCapabilities method retrieves the device capabilities to determine what operations the device can perform. The capabilities describe the methods of the device control that are supported by the media device.
helpviewer_keywords: ["GetCapabilities","GetCapabilities method [windows Media Device Manager]","GetCapabilities method [windows Media Device Manager]","IWMDMDeviceControl interface","IWMDMDeviceControl interface [windows Media Device Manager]","GetCapabilities method","IWMDMDeviceControl.GetCapabilities","IWMDMDeviceControl::GetCapabilities","IWMDMDeviceControlGetCapabilities","mswmdm/IWMDMDeviceControl::GetCapabilities","wmdm.iwmdmdevicecontrol_getcapabilities"]
old-location: wmdm\iwmdmdevicecontrol_getcapabilities.htm
tech.root: WMDM
ms.assetid: 61d0e44c-f1be-4837-a773-48c6c5278fe0
ms.date: 12/05/2018
ms.keywords: GetCapabilities, GetCapabilities method [windows Media Device Manager], GetCapabilities method [windows Media Device Manager],IWMDMDeviceControl interface, IWMDMDeviceControl interface [windows Media Device Manager],GetCapabilities method, IWMDMDeviceControl.GetCapabilities, IWMDMDeviceControl::GetCapabilities, IWMDMDeviceControlGetCapabilities, mswmdm/IWMDMDeviceControl::GetCapabilities, wmdm.iwmdmdevicecontrol_getcapabilities
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
 - IWMDMDeviceControl::GetCapabilities
 - mswmdm/IWMDMDeviceControl::GetCapabilities
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
 - IWMDMDeviceControl.GetCapabilities
---

# IWMDMDeviceControl::GetCapabilities


## -description

The <b>GetCapabilities</b> method retrieves the device capabilities to determine what operations the device can perform. The capabilities describe the methods of the device control that are supported by the media device.

## -parameters

### -param pdwCapabilitiesMask [out]

Pointer to a <b>DWORD</b> specifying the capabilities of the device. The following flags can be returned in this variable.

<table>
<tr>
<th>Flag
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>WMDM_DEVICECAP_CANPLAY</td>
<td>The media device can play MP3 audio.</td>
</tr>
<tr>
<td>WMDM_DEVICECAP_CANSTREAMPLAY</td>
<td>The media device can play streaming audio directly from the host computer.</td>
</tr>
<tr>
<td>WMDM_DEVICECAP_CANRECORD</td>
<td>The media device can record audio.</td>
</tr>
<tr>
<td>WMDM_DEVICECAP_CANSTREAMRECORD</td>
<td>The media device can record streaming audio directly to the host computer.</td>
</tr>
<tr>
<td>WMDM_DEVICECAP_CANPAUSE</td>
<td>The media device can pause during play or record operations.</td>
</tr>
<tr>
<td>WMDM_DEVICECAP_CANRESUME</td>
<td>The media device can resume an operation that was paused.</td>
</tr>
<tr>
<td>WMDM_DEVICECAP_CANSTOP</td>
<td>The media device can stop playing before the end of a file.</td>
</tr>
<tr>
<td>WMDM_DEVICECAP_CANSEEK</td>
<td>The media device can seek to a position other than the beginning of a file.</td>
</tr>
<tr>
<td>WMDM_DEVICECAP_HASSECURECLOCK</td>
<td>The media device has a secure clock.</td>
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

## -remarks

Currently, not many devices report their capabilities correctly.


#### Examples

The following C++ code retrieves the device capabilities.


```cpp

// Examine the device capabilities.
// Use some of these to enable or disable the application's
// user interface elements.
CComQIPtr<IWMDMDeviceControl> pDeviceControl(pIWMDMDevice);
if (pDeviceControl != NULL)
{
    DWORD caps = 0;
    hr = pDeviceControl->GetCapabilities(&caps);
    if (caps & WMDM_DEVICECAP_CANPLAY)
    {
        // TODO: Display a message indicating that the media device can play MP3 audio.
    }
    if (caps & WMDM_DEVICECAP_CANSTREAMPLAY)
    {
        // TODO: Display a message that the device can play audio directly from the host computer.
    }
    if (caps & WMDM_DEVICECAP_CANRECORD)
    {
        // TODO: Display a message that the device can record audio.
    }
    if (caps & WMDM_DEVICECAP_CANSTREAMRECORD)
    {
        // TODO: Display a message that the media device can record 
        // streaming audio directly to the host computer.
    }
    if (caps & WMDM_DEVICECAP_CANPAUSE)
    {
        // TODO: Display a message that the device can pause during play or record operations.
    }
    if (caps & WMDM_DEVICECAP_CANRESUME)
    {
        // TODO: Display a message that the device can resume an operation that was paused.
    }
    if (caps & WMDM_DEVICECAP_CANSTOP)
    {
        // TODO: Display a message that the device can stop playing before the end of a file.
    }
    if (caps & WMDM_DEVICECAP_CANSEEK)
    {
        // TODO: Display a message that the device can seek to a position 
        // other than the beginning of the file.
    }
    if (caps & WMDM_DEVICECAP_HASSECURECLOCK)
    {
        // TODO: Display a message indicating that the device has a secure clock.
    }
}

```

## -see-also

<a href="/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevicecontrol">IWMDMDeviceControl Interface</a>



<a href="/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmobjectinfo">IWMDMObjectInfo Interface</a>