---
UID: NF:imapi2.IWriteEngine2.put_StartingSectorsPerSecond
title: IWriteEngine2::put_StartingSectorsPerSecond (imapi2.h)
description: Sets the estimated number of sectors per second that the recording device can write to the media at the start of the writing process.
helpviewer_keywords: ["IWriteEngine2 interface [IMAPI]","put_StartingSectorsPerSecond method","IWriteEngine2.put_StartingSectorsPerSecond","IWriteEngine2::put_StartingSectorsPerSecond","imapi.iwriteengine2_put_startingsectorspersecond","imapi2/IWriteEngine2::put_StartingSectorsPerSecond","put_StartingSectorsPerSecond","put_StartingSectorsPerSecond method [IMAPI]","put_StartingSectorsPerSecond method [IMAPI]","IWriteEngine2 interface"]
old-location: imapi\iwriteengine2_put_startingsectorspersecond.htm
tech.root: imapi
ms.assetid: 80d6efdd-c3ce-4c6b-9bc2-7ad34c1dfb5e
ms.date: 12/05/2018
ms.keywords: IWriteEngine2 interface [IMAPI],put_StartingSectorsPerSecond method, IWriteEngine2.put_StartingSectorsPerSecond, IWriteEngine2::put_StartingSectorsPerSecond, imapi.iwriteengine2_put_startingsectorspersecond, imapi2/IWriteEngine2::put_StartingSectorsPerSecond, put_StartingSectorsPerSecond, put_StartingSectorsPerSecond method [IMAPI], put_StartingSectorsPerSecond method [IMAPI],IWriteEngine2 interface
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
 - IWriteEngine2::put_StartingSectorsPerSecond
 - imapi2/IWriteEngine2::put_StartingSectorsPerSecond
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
 - IWriteEngine2.put_StartingSectorsPerSecond
---

# IWriteEngine2::put_StartingSectorsPerSecond


## -description

Sets the estimated number of sectors per second that the recording device can write to the media at the start of the writing process.

## -parameters

### -param value [in]

Approximate number of sectors per second that the recording device can write to the media at the start of the writing process. The default is -1 for maximum speed.

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

This is used to optimize sleep time in the write engine.

## -see-also

<a href="/windows/desktop/api/imapi2/nn-imapi2-iwriteengine2">IWriteEngine2</a>



<a href="/windows/desktop/api/imapi2/nf-imapi2-iwriteengine2-get_bytespersector">IWriteEngine2::get_BytesPerSector</a>



<a href="/windows/desktop/api/imapi2/nf-imapi2-iwriteengine2-get_endingsectorspersecond">IWriteEngine2::get_EndingSectorsPerSecond</a>



<a href="/windows/desktop/api/imapi2/nf-imapi2-iwriteengine2-get_startingsectorspersecond">IWriteEngine2::get_StartingSectorsPerSecond</a>



<a href="/windows/desktop/api/imapi2/nf-imapi2-iwriteengine2-put_bytespersector">IWriteEngine2::put_BytesPerSector</a>



<a href="/windows/desktop/api/imapi2/nf-imapi2-iwriteengine2-put_endingsectorspersecond">IWriteEngine2::put_EndingSectorsPerSecond</a>