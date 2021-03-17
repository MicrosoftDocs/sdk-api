---
UID: NF:mmdeviceapi.IMMDevice.OpenPropertyStore
title: IMMDevice::OpenPropertyStore (mmdeviceapi.h)
description: The OpenPropertyStore method retrieves an interface to the device's property store.
helpviewer_keywords: ["IMMDevice interface [Core Audio]","OpenPropertyStore method","IMMDevice.OpenPropertyStore","IMMDevice::OpenPropertyStore","IMMDeviceOpenPropertyStore","OpenPropertyStore","OpenPropertyStore method [Core Audio]","OpenPropertyStore method [Core Audio]","IMMDevice interface","coreaudio.immdevice_openpropertystore","mmdeviceapi/IMMDevice::OpenPropertyStore"]
old-location: coreaudio\immdevice_openpropertystore.htm
tech.root: CoreAudio
ms.assetid: d13a5743-8b07-4876-ab9d-7a6bd60e7add
ms.date: 12/05/2018
ms.keywords: IMMDevice interface [Core Audio],OpenPropertyStore method, IMMDevice.OpenPropertyStore, IMMDevice::OpenPropertyStore, IMMDeviceOpenPropertyStore, OpenPropertyStore, OpenPropertyStore method [Core Audio], OpenPropertyStore method [Core Audio],IMMDevice interface, coreaudio.immdevice_openpropertystore, mmdeviceapi/IMMDevice::OpenPropertyStore
req.header: mmdeviceapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - IMMDevice::OpenPropertyStore
 - mmdeviceapi/IMMDevice::OpenPropertyStore
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mmdeviceapi.h
api_name:
 - IMMDevice.OpenPropertyStore
---

# IMMDevice::OpenPropertyStore


## -description

The <b>OpenPropertyStore</b> method retrieves an interface to the device's property store.

## -parameters

### -param stgmAccess [in]

The storage-access mode. This parameter specifies whether to open the property store in read mode, write mode, or read/write mode. Set this parameter to one of the following STGM constants:

STGM_READ

STGM_WRITE

STGM_READWRITE

The method permits a client running as an administrator to open a store for read-only, write-only, or read/write access. A client that is not running as an administrator is restricted to read-only access. For more information about STGM constants, see the Windows SDK documentation.

### -param ppProperties [out]

Pointer to a pointer variable into which the method writes the address of the <b>IPropertyStore</b> interface of the device's property store. Through this method, the caller obtains a counted reference to the interface. The caller is responsible for releasing the interface, when it is no longer needed, by calling the interface's <b>Release</b> method. If the <b>OpenPropertyStore</b> call fails,  <i>*ppProperties</i> is <b>NULL</b>. For more information about <b>IPropertyStore</b>, see the Windows SDK documentation.

## -returns

If the method succeeds, it returns S_OK. If it fails, possible return codes include, but are not limited to, the values shown in the following table.

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
Parameter <i>stgmAccess</i> is not a valid access mode.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
Parameter <i>ppProperties</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Out of memory.

</td>
</tr>
</table>

## -remarks

In general, the properties in the device's property store are read-only for clients that do not perform administrative, system, or service functions.

For code examples that call the <b>OpenPropertyStore</b> method, see the following topics:

<ul>
<li>
<a href="/windows/desktop/CoreAudio/device-properties">Device Properties</a>
</li>
<li>
<a href="/windows/desktop/CoreAudio/device-roles-for-directsound-applications">Device Roles for DirectSound Applications</a>
</li>
</ul>

## -see-also

<a href="/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immdevice">IMMDevice Interface</a>