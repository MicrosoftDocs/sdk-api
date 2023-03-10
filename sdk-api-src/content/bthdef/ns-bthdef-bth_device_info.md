---
UID: NS:bthdef._BTH_DEVICE_INFO
title: BTH_DEVICE_INFO (bthdef.h)
description: Stores information about a Bluetooth device.
helpviewer_keywords: ["*PBTH_DEVICE_INFO","*PBTH_DEVICE_INFO structure [Bluetooth]","BDIF_ADDRESS","BDIF_COD","BDIF_CONNECTED","BDIF_NAME","BDIF_PAIRED","BDIF_PERSONAL","BDIF_SSP_MITM_PROTECTED","BDIF_SSP_PAIRED","BDIF_SSP_SUPPORTED","BTH_DEVICE_INFO","BTH_DEVICE_INFO structure [Bluetooth]","COD_MAJOR_AUDIO","COD_MAJOR_COMPUTER","COD_MAJOR_IMAGING","COD_MAJOR_LAN_ACCESS","COD_MAJOR_MISCELLANEOUS","COD_MAJOR_PERIPHERAL","COD_MAJOR_PHONE","COD_MAJOR_UNCLASSIFIED","COD_SERVICE_AUDIO","COD_SERVICE_CAPTURING","COD_SERVICE_INFORMATION","COD_SERVICE_LIMITED","COD_SERVICE_NETWORKING","COD_SERVICE_OBJECT_XFER","COD_SERVICE_POSITIONING","COD_SERVICE_RENDERING","COD_SERVICE_TELEPHONY","bluetooth.bth_device_info","bthdef/*PBTH_DEVICE_INFO","bthdef/BTH_DEVICE_INFO"]
old-location: bluetooth\bth_device_info.htm
tech.root: bluetooth
ms.assetid: b0f2c1fe-1fa0-4816-8471-73fbbced529b
ms.date: 12/05/2018
ms.keywords: '*PBTH_DEVICE_INFO, *PBTH_DEVICE_INFO structure [Bluetooth], BDIF_ADDRESS, BDIF_COD, BDIF_CONNECTED, BDIF_NAME, BDIF_PAIRED, BDIF_PERSONAL, BDIF_SSP_MITM_PROTECTED, BDIF_SSP_PAIRED, BDIF_SSP_SUPPORTED, BTH_DEVICE_INFO, BTH_DEVICE_INFO structure [Bluetooth], COD_MAJOR_AUDIO, COD_MAJOR_COMPUTER, COD_MAJOR_IMAGING, COD_MAJOR_LAN_ACCESS, COD_MAJOR_MISCELLANEOUS, COD_MAJOR_PERIPHERAL, COD_MAJOR_PHONE, COD_MAJOR_UNCLASSIFIED, COD_SERVICE_AUDIO, COD_SERVICE_CAPTURING, COD_SERVICE_INFORMATION, COD_SERVICE_LIMITED, COD_SERVICE_NETWORKING, COD_SERVICE_OBJECT_XFER, COD_SERVICE_POSITIONING, COD_SERVICE_RENDERING, COD_SERVICE_TELEPHONY, bluetooth.bth_device_info, bthdef/*PBTH_DEVICE_INFO, bthdef/BTH_DEVICE_INFO'
req.header: bthdef.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP2 [desktop apps only]
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: BTH_DEVICE_INFO, *PBTH_DEVICE_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _BTH_DEVICE_INFO
 - bthdef/_BTH_DEVICE_INFO
 - PBTH_DEVICE_INFO
 - bthdef/PBTH_DEVICE_INFO
 - BTH_DEVICE_INFO
 - bthdef/BTH_DEVICE_INFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Bthdef.h
api_name:
 - BTH_DEVICE_INFO
---

# BTH_DEVICE_INFO structure


## -description

The <b>BTH_DEVICE_INFO</b> structure stores information about a Bluetooth device.

## -struct-fields

### -field flags

A combination of one or more of the  flags listed in the following table.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="BDIF_ADDRESS"></a><a id="bdif_address"></a><dl>
<dt><b>BDIF_ADDRESS</b></dt>
</dl>
</td>
<td width="60%">
The <b>address</b> member contains valid data.

</td>
</tr>
<tr>
<td width="40%"><a id="BDIF_COD"></a><a id="bdif_cod"></a><dl>
<dt><b>BDIF_COD</b></dt>
</dl>
</td>
<td width="60%">
The <b>classOfDevice</b> member contains valid data.

</td>
</tr>
<tr>
<td width="40%"><a id="BDIF_NAME"></a><a id="bdif_name"></a><dl>
<dt><b>BDIF_NAME</b></dt>
</dl>
</td>
<td width="60%">
The <b>name</b> member contains valid data.

</td>
</tr>
<tr>
<td width="40%"><a id="BDIF_PAIRED"></a><a id="bdif_paired"></a><dl>
<dt><b>BDIF_PAIRED</b></dt>
</dl>
</td>
<td width="60%">
The device is a remembered and authenticated device. The <b>BDIF_PERSONAL</b> flag is always set when this flag is set.

</td>
</tr>
<tr>
<td width="40%"><a id="BDIF_PERSONAL"></a><a id="bdif_personal"></a><dl>
<dt><b>BDIF_PERSONAL</b></dt>
</dl>
</td>
<td width="60%">
The device is a remembered device. If this flag is set and the <b>BDIF_PAIRED</b> flag is not set, the device is not authenticated.

</td>
</tr>
<tr>
<td width="40%"><a id="BDIF_CONNECTED"></a><a id="bdif_connected"></a><dl>
<dt><b>BDIF_CONNECTED</b></dt>
</dl>
</td>
<td width="60%">
The remote Bluetooth device is currently connected to the local radio.

</td>
</tr>
<tr>
<td width="40%"><a id="BDIF_SSP_SUPPORTED"></a><a id="bdif_ssp_supported"></a><dl>
<dt><b>BDIF_SSP_SUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
The device supports the use of Secure Simple Pairing (SSP).

</td>
</tr>
<tr>
<td width="40%"><a id="BDIF_SSP_PAIRED"></a><a id="bdif_ssp_paired"></a><dl>
<dt><b>BDIF_SSP_PAIRED</b></dt>
</dl>
</td>
<td width="60%">
The device is remembered and is authenticated using Secure Simple Pairing (SSP).

</td>
</tr>
<tr>
<td width="40%"><a id="BDIF_SSP_MITM_PROTECTED"></a><a id="bdif_ssp_mitm_protected"></a><dl>
<dt><b>BDIF_SSP_MITM_PROTECTED</b></dt>
</dl>
</td>
<td width="60%">
The device supports the use of Secure Simple Pairing (SSP) to protect against "Man in the Middle" attacks.

</td>
</tr>
</table>

### -field address

Address of the remote Bluetooth device.

### -field classOfDevice

Bit field that describes the device class of device (COD) of the remote device. The COD consists of the following four fields:

Format: retrieved using GET_COD_FORMAT(<b>classOfDevice</b>). The only format currently supported is COD_VERSION.



Major: retrieved using the GET_COD_MAJOR(<b>classOfDevice</b>). The following values are currently  defined, but the list is expected to expand.  Do not use the major class field to determine to which remote device to  connect.  A remote device may only have one major class code, and may not be the appropriate code for the given profile.

<a id="COD_MAJOR_MISCELLANEOUS"></a>
<a id="cod_major_miscellaneous"></a>


#### COD_MAJOR_MISCELLANEOUS

<a id="COD_MAJOR_COMPUTER"></a>
<a id="cod_major_computer"></a>


#### COD_MAJOR_COMPUTER

<a id="COD_MAJOR_PHONE"></a>
<a id="cod_major_phone"></a>


#### COD_MAJOR_PHONE

<a id="COD_MAJOR_LAN_ACCESS"></a>
<a id="cod_major_lan_access"></a>


#### COD_MAJOR_LAN_ACCESS

<a id="COD_MAJOR_AUDIO"></a>
<a id="cod_major_audio"></a>


#### COD_MAJOR_AUDIO

<a id="COD_MAJOR_PERIPHERAL"></a>
<a id="cod_major_peripheral"></a>


#### COD_MAJOR_PERIPHERAL

<a id="COD_MAJOR_IMAGING"></a>
<a id="cod_major_imaging"></a>


#### COD_MAJOR_IMAGING

<a id="COD_MAJOR_UNCLASSIFIED"></a>
<a id="cod_major_unclassified"></a>


#### COD_MAJOR_UNCLASSIFIED

Minor: retrieved using GET_COD_MINOR(<b>classOfDevice</b>). The minor code is specific to each major code, which defines how its minor code is formatted.  Some minor codes are strictly enumerated values; others are bit fields or a combination of bit fields and enumerated values.

Service hints: retrieved using the GET_COD_SERVICE(<b>classOfDevice</b>). Provides hints about the capability of the remote device.

<a id="COD_SERVICE_LIMITED"></a>
<a id="cod_service_limited"></a>


#### COD_SERVICE_LIMITED

<a id="COD_SERVICE_POSITIONING"></a>
<a id="cod_service_positioning"></a>


#### COD_SERVICE_POSITIONING

<a id="COD_SERVICE_NETWORKING"></a>
<a id="cod_service_networking"></a>


#### COD_SERVICE_NETWORKING

<a id="COD_SERVICE_RENDERING"></a>
<a id="cod_service_rendering"></a>


#### COD_SERVICE_RENDERING

<a id="COD_SERVICE_CAPTURING"></a>
<a id="cod_service_capturing"></a>


#### COD_SERVICE_CAPTURING

<a id="COD_SERVICE_OBJECT_XFER"></a>
<a id="cod_service_object_xfer"></a>


#### COD_SERVICE_OBJECT_XFER

<a id="COD_SERVICE_AUDIO"></a>
<a id="cod_service_audio"></a>


#### COD_SERVICE_AUDIO

<a id="COD_SERVICE_TELEPHONY"></a>
<a id="cod_service_telephony"></a>


#### COD_SERVICE_TELEPHONY

<a id="COD_SERVICE_INFORMATION"></a>
<a id="cod_service_information"></a>


#### COD_SERVICE_INFORMATION

### -field name

Name of the remote Bluetooth device, as reported by the device, encoded in UTF8.  The user may have locally provided a display name for the remote Bluetooth device; that name is overridden, and does not appear in this member; it is accessible only with a call to the 
<a href="/windows/desktop/api/bluetoothapis/nf-bluetoothapis-bluetoothgetdeviceinfo">BluetoothGetDeviceInfo</a> function.

## -see-also

<a href="/windows/desktop/api/ws2bth/ns-ws2bth-bth_query_device">BTH_QUERY_DEVICE</a>



<a href="/windows/desktop/api/ws2bth/ns-ws2bth-bth_query_service">BTH_QUERY_SERVICE</a>



<a href="/windows/desktop/api/ws2bth/ns-ws2bth-bth_set_service">BTH_SET_SERVICE</a>



<a href="/windows/desktop/api/bluetoothapis/nf-bluetoothapis-bluetoothgetdeviceinfo">BluetoothGetDeviceInfo</a>