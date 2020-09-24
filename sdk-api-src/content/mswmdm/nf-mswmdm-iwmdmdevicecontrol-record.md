---
UID: NF:mswmdm.IWMDMDeviceControl.Record
title: IWMDMDeviceControl::Record (mswmdm.h)
description: The Record method begins recording from the device's external record input at the current seek position. The IWMDMDeviceControl::Seek method must be called first.
helpviewer_keywords: ["IWMDMDeviceControl interface [windows Media Device Manager]","Record method","IWMDMDeviceControl.Record","IWMDMDeviceControl::Record","IWMDMDeviceControlRecord","Record","Record method [windows Media Device Manager]","Record method [windows Media Device Manager]","IWMDMDeviceControl interface","mswmdm/IWMDMDeviceControl::Record","wmdm.iwmdmdevicecontrol_record"]
old-location: wmdm\iwmdmdevicecontrol_record.htm
tech.root: WMDM
ms.assetid: a9372ce9-e339-4664-9e12-4feae29529dc
ms.date: 12/05/2018
ms.keywords: IWMDMDeviceControl interface [windows Media Device Manager],Record method, IWMDMDeviceControl.Record, IWMDMDeviceControl::Record, IWMDMDeviceControlRecord, Record, Record method [windows Media Device Manager], Record method [windows Media Device Manager],IWMDMDeviceControl interface, mswmdm/IWMDMDeviceControl::Record, wmdm.iwmdmdevicecontrol_record
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
 - IWMDMDeviceControl::Record
 - mswmdm/IWMDMDeviceControl::Record
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
 - IWMDMDeviceControl.Record
---

# IWMDMDeviceControl::Record


## -description

The <b>Record</b> method begins recording from the device's external record input at the current seek position. The <b>IWMDMDeviceControl::Seek</b> method must be called first.

## -parameters

### -param pFormat [in]

Pointer to a <a href="/windows/desktop/WMDM/-waveformatex">_WAVEFORMATEX</a> structure specifying the format in which the data must be recorded.

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
<dt><b>E_BUSY</b></dt>
</dl>
</td>
<td width="60%">
The device is already performing an operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WMDM_E_NOTSUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
The record function is not implemented on this device.

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

This method is used to invoke both device recording (recording of an audio track to be stored on the media device) and streaming audio data from the media device to be recorded on the computer. The <a href="/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevicecontrol-seek">Seek</a> method determines which form of recording occurs.

Some devices do not support either type of recording. The <a href="/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevicecontrol-getcapabilities">GetCapabilities</a> method must be called before you start recording. If an unsupported type of recording is attempted, this method returns WMDM_E_NOTSUPPORTED.

An argument can be supplied for the <i>pFormat</i> parameter to specify an audio format for recording. To determine the formats supported by the device, see <a href="/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice-getformatsupport">GetFormatSupport</a>. If the <i>pFormat</i> parameter is set to <b>NULL</b>, the device records audio data in the default format.

When you use device recording, you must enumerate the storage medium contents to find the new object after the record operation is finished.

## -see-also

<a href="/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice-getformatsupport">IWMDMDevice::GetFormatSupport</a>



<a href="/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevicecontrol">IWMDMDeviceControl Interface</a>



<a href="/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevicecontrol-getcapabilities">IWMDMDeviceControl::GetCapabilities</a>



<a href="/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevicecontrol-seek">IWMDMDeviceControl::Seek</a>



<a href="/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmobjectinfo">IWMDMObjectInfo Interface</a>



<a href="/windows/desktop/WMDM/-waveformatex">_WAVEFORMATEX</a>