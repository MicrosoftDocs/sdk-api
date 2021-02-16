---
UID: NF:imapi2.IWriteEngine2.get_BytesPerSector
title: IWriteEngine2::get_BytesPerSector (imapi2.h)
description: Retrieves the number of bytes to use for each sector during writing. The returned value indicates what the value previously set with IWriteEngine2::put_BytesPerSector, and does not return a current bytes per sector value for media.
helpviewer_keywords: ["IWriteEngine2 interface [IMAPI]","get_BytesPerSector method","IWriteEngine2.get_BytesPerSector","IWriteEngine2::get_BytesPerSector","get_BytesPerSector","get_BytesPerSector method [IMAPI]","get_BytesPerSector method [IMAPI]","IWriteEngine2 interface","imapi.iwriteengine2_get_bytespersector","imapi2/IWriteEngine2::get_BytesPerSector"]
old-location: imapi\iwriteengine2_get_bytespersector.htm
tech.root: imapi
ms.assetid: ee48368c-e9bc-4ac7-97cf-a2bdc2a05d22
ms.date: 12/05/2018
ms.keywords: IWriteEngine2 interface [IMAPI],get_BytesPerSector method, IWriteEngine2.get_BytesPerSector, IWriteEngine2::get_BytesPerSector, get_BytesPerSector, get_BytesPerSector method [IMAPI], get_BytesPerSector method [IMAPI],IWriteEngine2 interface, imapi.iwriteengine2_get_bytespersector, imapi2/IWriteEngine2::get_BytesPerSector
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
 - IWriteEngine2::get_BytesPerSector
 - imapi2/IWriteEngine2::get_BytesPerSector
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
 - IWriteEngine2.get_BytesPerSector
---

# IWriteEngine2::get_BytesPerSector


## -description

Retrieves the number of bytes to use for each sector during writing. The returned value indicates what the value previously set with <a href="/windows/desktop/api/imapi2/nf-imapi2-iwriteengine2-put_bytespersector">IWriteEngine2::put_BytesPerSector</a>, and does not return a current bytes per sector value for media.

## -parameters

### -param value [out]

Number of bytes to use for each sector during writing.

<div class="alert"><b>Note</b>  If <a href="/windows/desktop/api/imapi2/nf-imapi2-iwriteengine2-put_bytespersector">IWriteEngine2::put_BytesPerSector</a> has not been called, this parameter will indicate a value of  '-1'.
</div>
<div> </div>

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



<a href="/windows/desktop/api/imapi2/nf-imapi2-iwriteengine2-get_endingsectorspersecond">IWriteEngine2::get_EndingSectorsPerSecond</a>



<a href="/windows/desktop/api/imapi2/nf-imapi2-iwriteengine2-get_startingsectorspersecond">IWriteEngine2::get_StartingSectorsPerSecond</a>



<a href="/windows/desktop/api/imapi2/nf-imapi2-iwriteengine2-put_bytespersector">IWriteEngine2::put_BytesPerSector</a>



<a href="/windows/desktop/api/imapi2/nf-imapi2-iwriteengine2-put_endingsectorspersecond">IWriteEngine2::put_EndingSectorsPerSecond</a>



<a href="/windows/desktop/api/imapi2/nf-imapi2-iwriteengine2-put_startingsectorspersecond">IWriteEngine2::put_StartingSectorsPerSecond</a>