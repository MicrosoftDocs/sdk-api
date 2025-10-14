---
UID: NF:bits.IBackgroundCopyJob.GetDescription
title: IBackgroundCopyJob::GetDescription (bits.h)
description: Retrieves the description of the job.
helpviewer_keywords: ["GetDescription","GetDescription method [BITS]","GetDescription method [BITS]","IBackgroundCopyJob interface","IBackgroundCopyJob interface [BITS]","GetDescription method","IBackgroundCopyJob.GetDescription","IBackgroundCopyJob::GetDescription","_drz_ibackgroundcopyjob_getdescription","bits.ibackgroundcopyjob_getdescription","bits/IBackgroundCopyJob::GetDescription"]
old-location: bits\ibackgroundcopyjob_getdescription.htm
tech.root: Bits
ms.assetid: 1a791390-2bd8-4732-98a2-74f740cfd822
ms.date: 12/05/2018
ms.keywords: GetDescription, GetDescription method [BITS], GetDescription method [BITS],IBackgroundCopyJob interface, IBackgroundCopyJob interface [BITS],GetDescription method, IBackgroundCopyJob.GetDescription, IBackgroundCopyJob::GetDescription, _drz_ibackgroundcopyjob_getdescription, bits.ibackgroundcopyjob_getdescription, bits/IBackgroundCopyJob::GetDescription
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
 - IBackgroundCopyJob::GetDescription
 - bits/IBackgroundCopyJob::GetDescription
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
 - IBackgroundCopyJob.GetDescription
---

# IBackgroundCopyJob::GetDescription


## -description

Retrieves the description of the job.

## -parameters

### -param pVal [out]

Null-terminated string that contains a short description of the job. Call the 
<a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a> function to free <i>ppDescription</i> when done.

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
Description of the job was successfully retrieved.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The parameter, <i>ppDescription</i>, cannot be <b>NULL</b>.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/bits/nf-bits-ibackgroundcopyjob-setdescription">IBackgroundCopyJob::SetDescription</a>