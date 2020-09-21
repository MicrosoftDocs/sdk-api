---
UID: NF:imapi2.IDiscRecorder2Ex.GetDeviceDescriptor
title: IDiscRecorder2Ex::GetDeviceDescriptor (imapi2.h)
description: Retrieves the device descriptor for the device.
helpviewer_keywords: ["GetDeviceDescriptor","GetDeviceDescriptor method [IMAPI]","GetDeviceDescriptor method [IMAPI]","IDiscRecorder2Ex interface","IDiscRecorder2Ex interface [IMAPI]","GetDeviceDescriptor method","IDiscRecorder2Ex.GetDeviceDescriptor","IDiscRecorder2Ex::GetDeviceDescriptor","imapi.idiscrecorder2ex_getdevicedescriptor","imapi2/IDiscRecorder2Ex::GetDeviceDescriptor"]
old-location: imapi\idiscrecorder2ex_getdevicedescriptor.htm
tech.root: imapi
ms.assetid: c0c22ce6-daf4-4218-afce-c773d607638b
ms.date: 12/05/2018
ms.keywords: GetDeviceDescriptor, GetDeviceDescriptor method [IMAPI], GetDeviceDescriptor method [IMAPI],IDiscRecorder2Ex interface, IDiscRecorder2Ex interface [IMAPI],GetDeviceDescriptor method, IDiscRecorder2Ex.GetDeviceDescriptor, IDiscRecorder2Ex::GetDeviceDescriptor, imapi.idiscrecorder2ex_getdevicedescriptor, imapi2/IDiscRecorder2Ex::GetDeviceDescriptor
req.header: imapi2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Imapi2.idl
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
 - IDiscRecorder2Ex::GetDeviceDescriptor
 - imapi2/IDiscRecorder2Ex::GetDeviceDescriptor
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - imapi2.h
api_name:
 - IDiscRecorder2Ex.GetDeviceDescriptor
---

# IDiscRecorder2Ex::GetDeviceDescriptor


## -description

Retrieves the device descriptor for the device.

## -parameters

### -param data [out]

Data buffer that contains the descriptor of the storage device. For details of the contents of the data buffer, see the <b>STORAGE_DEVICE_DESCRIPTOR</b> structure in the DDK

When done, call the <b>CoTaskMemFree</b> function to free the memory.

### -param byteSize [out]

Size, in bytes, of the data buffer.

## -returns

S_OK is returned on success, but other success codes may be returned as a result of implementation. The following error codes are commonly returned on operation failure, but do not represent the only possible error values:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
Pointer is not valid.

Value: 0x80004003

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
Unspecified failure.

Value: 0x80004005

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Failed to allocate the required memory.

Value: 0x8007000E

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/imapi2/nn-imapi2-idiscrecorder2ex">IDiscRecorder2Ex</a>