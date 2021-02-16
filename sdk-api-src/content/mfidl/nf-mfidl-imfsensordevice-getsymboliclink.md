---
UID: NF:mfidl.IMFSensorDevice.GetSymbolicLink
title: IMFSensorDevice::GetSymbolicLink (mfidl.h)
description: Gets the symbolic link name of the sensor device.
helpviewer_keywords: ["GetSymbolicLink","GetSymbolicLink method [Media Foundation]","GetSymbolicLink method [Media Foundation]","IMFSensorDevice interface","IMFSensorDevice interface [Media Foundation]","GetSymbolicLink method","IMFSensorDevice.GetSymbolicLink","IMFSensorDevice::GetSymbolicLink","mf.imfsensordevice_getsymboliclink","mfidl/IMFSensorDevice::GetSymbolicLink"]
old-location: mf\imfsensordevice_getsymboliclink.htm
tech.root: mf
ms.assetid: F9244454-DF1D-4A3D-8A63-830A8422AFA2
ms.date: 12/05/2018
ms.keywords: GetSymbolicLink, GetSymbolicLink method [Media Foundation], GetSymbolicLink method [Media Foundation],IMFSensorDevice interface, IMFSensorDevice interface [Media Foundation],GetSymbolicLink method, IMFSensorDevice.GetSymbolicLink, IMFSensorDevice::GetSymbolicLink, mf.imfsensordevice_getsymboliclink, mfidl/IMFSensorDevice::GetSymbolicLink
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1607 [desktop apps only]
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
req.lib: Mfplat.lib; Mfplat.dll
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFSensorDevice::GetSymbolicLink
 - mfidl/IMFSensorDevice::GetSymbolicLink
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfplat.lib
 - mfplat.dll
 - mfplat.dll
 - mfplat.dll.dll
api_name:
 - IMFSensorDevice.GetSymbolicLink
---

# IMFSensorDevice::GetSymbolicLink


## -description

Gets the symbolic link name of the sensor device.

## -parameters

### -param SymbolicLink [out]

Buffer of <i>cchSymbolicLink</i> characters where the symbolic link name will be written.  The buffer must be large enough to account for the null terminator.

### -param cchSymbolicLink [in]

Number of characters available in <i>SymbolicLink</i> buffer.

### -param pcchWritten [out]

Output parameter containing the number of characters written to <i>SymbolicLink</i>.  This includes the null terminator.  If <i>SymbolicLink</i> is null and <i>cchSymbolicLink</i> is 0, <i>pcchWritten</i> will contain the number of characters needed (including the null terminator) to store the symbolic link name.

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
<dt><b>ERROR_INSUFFICIENT_BUFFER</b></dt>
</dl>
</td>
<td width="60%">
The buffer provided in the <i>SymbolicLink</i> parameter is not large enough to contain the symbolic link name, including the null terminator.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_NOT_INITIALIZED</b></dt>
</dl>
</td>
<td width="60%">
The sensor device has not been initialized.

</td>
</tr>
</table>

## -remarks

Depending on the type of device, which is defined by a member of the <a href="/windows/win32/api/mfidl/ne-mfidl-mfsensordevicetype">MFSensorDeviceType</a> enumeration and can be obtained by calling <a href="/windows/desktop/api/mfidl/nf-mfidl-imfsensordevice-getdevicetype">GetDeviceType</a>, the resulting symbolic name may be a valid device symbolic name or a provider URL.  The caller should not attempt to parse the name and should treat it as opaque data.

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfsensordevice">IMFSensorDevice</a>