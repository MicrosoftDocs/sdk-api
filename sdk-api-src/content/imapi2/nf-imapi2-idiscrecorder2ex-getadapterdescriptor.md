---
UID: NF:imapi2.IDiscRecorder2Ex.GetAdapterDescriptor
title: IDiscRecorder2Ex::GetAdapterDescriptor (imapi2.h)
description: Retrieves the adapter descriptor for the device.
helpviewer_keywords: ["GetAdapterDescriptor","GetAdapterDescriptor method [IMAPI]","GetAdapterDescriptor method [IMAPI]","IDiscRecorder2Ex interface","IDiscRecorder2Ex interface [IMAPI]","GetAdapterDescriptor method","IDiscRecorder2Ex.GetAdapterDescriptor","IDiscRecorder2Ex::GetAdapterDescriptor","imapi.idiscrecorder2ex_getadapterdescriptor","imapi2/IDiscRecorder2Ex::GetAdapterDescriptor"]
old-location: imapi\idiscrecorder2ex_getadapterdescriptor.htm
tech.root: imapi
ms.assetid: 3922243c-97cf-43e3-a437-a5157ed73559
ms.date: 12/05/2018
ms.keywords: GetAdapterDescriptor, GetAdapterDescriptor method [IMAPI], GetAdapterDescriptor method [IMAPI],IDiscRecorder2Ex interface, IDiscRecorder2Ex interface [IMAPI],GetAdapterDescriptor method, IDiscRecorder2Ex.GetAdapterDescriptor, IDiscRecorder2Ex::GetAdapterDescriptor, imapi.idiscrecorder2ex_getadapterdescriptor, imapi2/IDiscRecorder2Ex::GetAdapterDescriptor
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
 - IDiscRecorder2Ex::GetAdapterDescriptor
 - imapi2/IDiscRecorder2Ex::GetAdapterDescriptor
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
 - IDiscRecorder2Ex.GetAdapterDescriptor
---

# IDiscRecorder2Ex::GetAdapterDescriptor


## -description

Retrieves the adapter descriptor for the device.

## -parameters

### -param data [out]

Data buffer that contains the descriptor of the storage adapter. For details of the contents of the data buffer, see the <b>STORAGE_ADAPTER_DESCRIPTOR</b> structure in the DDK

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
</table>

## -see-also

<a href="/windows/desktop/api/imapi2/nn-imapi2-idiscrecorder2ex">IDiscRecorder2Ex</a>