---
UID: NF:mswmdm.IWMDeviceManager2.GetDeviceFromCanonicalName
title: IWMDeviceManager2::GetDeviceFromCanonicalName (mswmdm.h)
description: The GetDeviceFromCanonicalName method retrieves an IWMDMDevice interface for a device with a specified canonical name. You can retrieve a device's canonical name by calling IWMDMDevice2::GetCanonicalName.
helpviewer_keywords: ["GetDeviceFromCanonicalName","GetDeviceFromCanonicalName method [windows Media Device Manager]","GetDeviceFromCanonicalName method [windows Media Device Manager]","IWMDeviceManager2 interface","IWMDeviceManager2 interface [windows Media Device Manager]","GetDeviceFromCanonicalName method","IWMDeviceManager2.GetDeviceFromCanonicalName","IWMDeviceManager2::GetDeviceFromCanonicalName","IWMDeviceManager2GetDevicesFromCanonicalName","mswmdm/IWMDeviceManager2::GetDeviceFromCanonicalName","wmdm.iwmdevicemanager2__getdevicefromcanonicalname"]
old-location: wmdm\iwmdevicemanager2__getdevicefromcanonicalname.htm
tech.root: WMDM
ms.assetid: cfa0fe8d-668a-443b-be50-cf1f83362a14
ms.date: 12/05/2018
ms.keywords: GetDeviceFromCanonicalName, GetDeviceFromCanonicalName method [windows Media Device Manager], GetDeviceFromCanonicalName method [windows Media Device Manager],IWMDeviceManager2 interface, IWMDeviceManager2 interface [windows Media Device Manager],GetDeviceFromCanonicalName method, IWMDeviceManager2.GetDeviceFromCanonicalName, IWMDeviceManager2::GetDeviceFromCanonicalName, IWMDeviceManager2GetDevicesFromCanonicalName, mswmdm/IWMDeviceManager2::GetDeviceFromCanonicalName, wmdm.iwmdevicemanager2__getdevicefromcanonicalname
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
 - IWMDeviceManager2::GetDeviceFromCanonicalName
 - mswmdm/IWMDeviceManager2::GetDeviceFromCanonicalName
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
 - IWMDeviceManager2.GetDeviceFromCanonicalName
---

# IWMDeviceManager2::GetDeviceFromCanonicalName


## -description

The <b>GetDeviceFromCanonicalName</b> method retrieves an <b>IWMDMDevice</b> interface for a device with a specified canonical name. You can retrieve a device's canonical name by calling <a href="/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice2-getcanonicalname">IWMDMDevice2::GetCanonicalName</a>.

## -parameters

### -param pwszCanonicalName

A wide-character, <b>null</b>-terminated string specifying the canonical name of the device.

### -param ppDevice

Pointer to a pointer to the <a href="/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice">IWMDMDevice</a> interface of the device object with the specified canonical name. The caller must release this interface when done with it.

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>pwszCanonicalName</i> or <i>ppDeviceArray</i> parameter is an invalid or <b>NULL</b> pointer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
There is no connected device found with canonical name <i>pwszCanonicalName</i>.

</td>
</tr>
</table>

## -remarks

This method can be useful if an application implements <a href="/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmnotification">IWMDMNotification</a>, which sends a canonical name notification when a device connects or disconnects from the computer.

## -see-also

<a href="/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice2">IWMDMDevice2 Interface</a>



<a href="/windows/desktop/api/mswmdm/nn-mswmdm-iwmdevicemanager2">IWMDeviceManager2 Interface</a>