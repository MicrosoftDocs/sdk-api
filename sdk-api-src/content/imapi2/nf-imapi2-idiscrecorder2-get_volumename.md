---
UID: NF:imapi2.IDiscRecorder2.get_VolumeName
title: IDiscRecorder2::get_VolumeName (imapi2.h)
description: Retrieves the unique volume name associated with the device.
helpviewer_keywords: ["IDiscRecorder2 interface [IMAPI]","get_VolumeName method","IDiscRecorder2.get_VolumeName","IDiscRecorder2::get_VolumeName","get_VolumeName","get_VolumeName method [IMAPI]","get_VolumeName method [IMAPI]","IDiscRecorder2 interface","imapi.idiscrecorder2_get_volumename","imapi2/IDiscRecorder2::get_VolumeName"]
old-location: imapi\idiscrecorder2_get_volumename.htm
tech.root: imapi
ms.assetid: 953f291d-a1b8-4cad-8ddf-59e251de65f2
ms.date: 12/05/2018
ms.keywords: IDiscRecorder2 interface [IMAPI],get_VolumeName method, IDiscRecorder2.get_VolumeName, IDiscRecorder2::get_VolumeName, get_VolumeName, get_VolumeName method [IMAPI], get_VolumeName method [IMAPI],IDiscRecorder2 interface, imapi.idiscrecorder2_get_volumename, imapi2/IDiscRecorder2::get_VolumeName
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
 - IDiscRecorder2::get_VolumeName
 - imapi2/IDiscRecorder2::get_VolumeName
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
 - IDiscRecorder2.get_VolumeName
---

# IDiscRecorder2::get_VolumeName


## -description

Retrieves the unique volume name associated with the device.

## -parameters

### -param value [out]

String that contains the unique volume name associated with the device.

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

## -remarks

To retrieve the drive letter assignment, call the <a href="/windows/desktop/api/imapi2/nf-imapi2-idiscrecorder2-get_volumepathnames">IDiscRecorder2::get_VolumePathNames</a> method.

## -see-also

<a href="/windows/desktop/api/imapi2/nn-imapi2-idiscrecorder2">IDiscRecorder2</a>