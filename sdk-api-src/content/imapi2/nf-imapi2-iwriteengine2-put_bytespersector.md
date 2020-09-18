---
UID: NF:imapi2.IWriteEngine2.put_BytesPerSector
title: IWriteEngine2::put_BytesPerSector (imapi2.h)
description: Sets the number of bytes to use for each sector during writing.
helpviewer_keywords: ["IWriteEngine2 interface [IMAPI]","put_BytesPerSector method","IWriteEngine2.put_BytesPerSector","IWriteEngine2::put_BytesPerSector","imapi.iwriteengine2_put_bytespersector","imapi2/IWriteEngine2::put_BytesPerSector","put_BytesPerSector","put_BytesPerSector method [IMAPI]","put_BytesPerSector method [IMAPI]","IWriteEngine2 interface"]
old-location: imapi\iwriteengine2_put_bytespersector.htm
tech.root: imapi
ms.assetid: aac64c0a-4304-4a20-822e-4aa247d3d9e8
ms.date: 12/05/2018
ms.keywords: IWriteEngine2 interface [IMAPI],put_BytesPerSector method, IWriteEngine2.put_BytesPerSector, IWriteEngine2::put_BytesPerSector, imapi.iwriteengine2_put_bytespersector, imapi2/IWriteEngine2::put_BytesPerSector, put_BytesPerSector, put_BytesPerSector method [IMAPI], put_BytesPerSector method [IMAPI],IWriteEngine2 interface
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
 - IWriteEngine2::put_BytesPerSector
 - imapi2/IWriteEngine2::put_BytesPerSector
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
 - IWriteEngine2.put_BytesPerSector
---

# IWriteEngine2::put_BytesPerSector


## -description

Sets the number of bytes to use for each sector during writing.

## -parameters

### -param value [in]

Number of bytes to use for each sector during writing. The minimum size is 1 byte and the maximum is MAXLONG bytes. Typically, this value is 2,048 bytes for CD media, although any arbitrary size is supported (such as 2352 or 2448). This value is limited to the <a href="/windows/desktop/api/imapi2/nf-imapi2-idiscrecorder2ex-getmaximumpagealignedtransfersize">IDiscRecorder2Ex::GetMaximumPageAlignedTransferSize</a>, which is typically 65,536 (64K) bytes.

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One or more arguments are not valid.

Value: 0x80070057

</td>
</tr>
</table>

## -remarks

You must specify a logical block size.

## -see-also

<a href="/windows/desktop/api/imapi2/nn-imapi2-iwriteengine2">IWriteEngine2</a>



<a href="/windows/desktop/api/imapi2/nf-imapi2-iwriteengine2-get_bytespersector">IWriteEngine2::get_BytesPerSector</a>



<a href="/windows/desktop/api/imapi2/nf-imapi2-iwriteengine2-get_endingsectorspersecond">IWriteEngine2::get_EndingSectorsPerSecond</a>



<a href="/windows/desktop/api/imapi2/nf-imapi2-iwriteengine2-get_startingsectorspersecond">IWriteEngine2::get_StartingSectorsPerSecond</a>



<a href="/windows/desktop/api/imapi2/nf-imapi2-iwriteengine2-put_endingsectorspersecond">IWriteEngine2::put_EndingSectorsPerSecond</a>



<a href="/windows/desktop/api/imapi2/nf-imapi2-iwriteengine2-put_startingsectorspersecond">IWriteEngine2::put_StartingSectorsPerSecond</a>