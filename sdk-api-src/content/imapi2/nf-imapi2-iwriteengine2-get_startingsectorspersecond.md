---
UID: NF:imapi2.IWriteEngine2.get_StartingSectorsPerSecond
title: IWriteEngine2::get_StartingSectorsPerSecond (imapi2.h)
description: Retrieves the estimated number of sectors per second that the recording device can write to the media at the start of the writing process.
helpviewer_keywords: ["IWriteEngine2 interface [IMAPI]","get_StartingSectorsPerSecond method","IWriteEngine2.get_StartingSectorsPerSecond","IWriteEngine2::get_StartingSectorsPerSecond","get_StartingSectorsPerSecond","get_StartingSectorsPerSecond method [IMAPI]","get_StartingSectorsPerSecond method [IMAPI]","IWriteEngine2 interface","imapi.iwriteengine2_get_startingsectorspersecond","imapi2/IWriteEngine2::get_StartingSectorsPerSecond"]
old-location: imapi\iwriteengine2_get_startingsectorspersecond.htm
tech.root: imapi
ms.assetid: 335da519-7378-469d-83dc-7c6a265fe67b
ms.date: 12/05/2018
ms.keywords: IWriteEngine2 interface [IMAPI],get_StartingSectorsPerSecond method, IWriteEngine2.get_StartingSectorsPerSecond, IWriteEngine2::get_StartingSectorsPerSecond, get_StartingSectorsPerSecond, get_StartingSectorsPerSecond method [IMAPI], get_StartingSectorsPerSecond method [IMAPI],IWriteEngine2 interface, imapi.iwriteengine2_get_startingsectorspersecond, imapi2/IWriteEngine2::get_StartingSectorsPerSecond
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
 - IWriteEngine2::get_StartingSectorsPerSecond
 - imapi2/IWriteEngine2::get_StartingSectorsPerSecond
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
 - IWriteEngine2.get_StartingSectorsPerSecond
---

# IWriteEngine2::get_StartingSectorsPerSecond


## -description

Retrieves the estimated number of sectors per second that the recording device can write to the media at the start of the writing process.

## -parameters

### -param value [out]

Approximate number of sectors per second that the recording device can write to the media at the start of the writing process.

A value of -1 indicates maximum speed.

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
</table>

## -see-also

<a href="/windows/desktop/api/imapi2/nn-imapi2-iwriteengine2">IWriteEngine2</a>



<a href="/windows/desktop/api/imapi2/nf-imapi2-iwriteengine2-get_bytespersector">IWriteEngine2::get_BytesPerSector</a>



<a href="/windows/desktop/api/imapi2/nf-imapi2-iwriteengine2-get_endingsectorspersecond">IWriteEngine2::get_EndingSectorsPerSecond</a>



<a href="/windows/desktop/api/imapi2/nf-imapi2-iwriteengine2-put_bytespersector">IWriteEngine2::put_BytesPerSector</a>



<a href="/windows/desktop/api/imapi2/nf-imapi2-iwriteengine2-put_endingsectorspersecond">IWriteEngine2::put_EndingSectorsPerSecond</a>



<a href="/windows/desktop/api/imapi2/nf-imapi2-iwriteengine2-put_startingsectorspersecond">IWriteEngine2::put_StartingSectorsPerSecond</a>