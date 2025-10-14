---
UID: NF:bits.IBackgroundCopyJob.SetDescription
title: IBackgroundCopyJob::SetDescription (bits.h)
description: Provides a description of the job.
helpviewer_keywords: ["IBackgroundCopyJob interface [BITS]","SetDescription method","IBackgroundCopyJob.SetDescription","IBackgroundCopyJob::SetDescription","SetDescription","SetDescription method [BITS]","SetDescription method [BITS]","IBackgroundCopyJob interface","_drz_ibackgroundcopyjob_setdescription","bits.ibackgroundcopyjob_setdescription","bits/IBackgroundCopyJob::SetDescription"]
old-location: bits\ibackgroundcopyjob_setdescription.htm
tech.root: Bits
ms.assetid: 9148ec9b-7a03-4bb3-9644-e52f6cd13073
ms.date: 12/05/2018
ms.keywords: IBackgroundCopyJob interface [BITS],SetDescription method, IBackgroundCopyJob.SetDescription, IBackgroundCopyJob::SetDescription, SetDescription, SetDescription method [BITS], SetDescription method [BITS],IBackgroundCopyJob interface, _drz_ibackgroundcopyjob_setdescription, bits.ibackgroundcopyjob_setdescription, bits/IBackgroundCopyJob::SetDescription
req.header: bits.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP
req.target-min-winversvr: Windows Server 2003
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Bits.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Bits.lib
req.dll: QmgrPrxy.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IBackgroundCopyJob::SetDescription
 - bits/IBackgroundCopyJob::SetDescription
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - QmgrPrxy.dll
api_name:
 - IBackgroundCopyJob.SetDescription
---

# IBackgroundCopyJob::SetDescription


## -description

Provides a description of the job.

## -parameters

### -param Val [in]

Null-terminated string that provides additional information about the job. The length of the string is limited to 1,024 characters, not including the null terminator.

## -returns

This method returns the following <b>HRESULT</b> values, as well as others.

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
Description of the job was successfully set.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>pDescription</i> parameter cannot be <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>BG_E_STRING_TOO_LONG</b></dt>
</dl>
</td>
<td width="60%">
The description exceeds 1,024 characters.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>BG_E_INVALID_STATE</b></dt>
</dl>
</td>
<td width="60%">
The state of the job cannot be BG_JOB_STATE_CANCELLED or BG_JOB_STATE_ACKNOWLEDGED.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/bits/nf-bits-ibackgroundcopyjob-getdescription">IBackgroundCopyJob::GetDescription</a>