---
UID: NF:bits2_5.IBackgroundCopyJobHttpOptions.GetCustomHeaders
title: IBackgroundCopyJobHttpOptions::GetCustomHeaders (bits2_5.h)
description: Retrieves the custom headers set by an earlier call to IBackgroundCopyJobHttpOptions::SetCustomHeaders (that is, headers which BITS will be sending to the remote, not headers which BITS receives from the remote).
helpviewer_keywords: ["GetCustomHeaders","GetCustomHeaders method [BITS]","GetCustomHeaders method [BITS]","IBackgroundCopyJobHttpOptions interface","IBackgroundCopyJobHttpOptions interface [BITS]","GetCustomHeaders method","IBackgroundCopyJobHttpOptions.GetCustomHeaders","IBackgroundCopyJobHttpOptions::GetCustomHeaders","bits.ibackgroundcopyjobhttpoptions_getcustomheaders","bits2_5/IBackgroundCopyJobHttpOptions::GetCustomHeaders"]
old-location: bits\ibackgroundcopyjobhttpoptions_getcustomheaders.htm
tech.root: Bits
ms.assetid: 8be6e9ec-7c74-44ff-94d7-a1a1d7fb18e9
ms.date: 12/05/2018
ms.keywords: GetCustomHeaders, GetCustomHeaders method [BITS], GetCustomHeaders method [BITS],IBackgroundCopyJobHttpOptions interface, IBackgroundCopyJobHttpOptions interface [BITS],GetCustomHeaders method, IBackgroundCopyJobHttpOptions.GetCustomHeaders, IBackgroundCopyJobHttpOptions::GetCustomHeaders, bits.ibackgroundcopyjobhttpoptions_getcustomheaders, bits2_5/IBackgroundCopyJobHttpOptions::GetCustomHeaders
req.header: bits2_5.h
req.include-header: Bits.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Bits2_5.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Bits.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IBackgroundCopyJobHttpOptions::GetCustomHeaders
 - bits2_5/IBackgroundCopyJobHttpOptions::GetCustomHeaders
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Bits.lib
 - Bits.dll
api_name:
 - IBackgroundCopyJobHttpOptions.GetCustomHeaders
---

# IBackgroundCopyJobHttpOptions::GetCustomHeaders


## -description

Retrieves the custom headers set by an earlier call to<a href="/windows/desktop/api/bits2_5/nf-bits2_5-ibackgroundcopyjobhttpoptions-setcustomheaders"> IBackgroundCopyJobHttpOptions::SetCustomHeaders</a> (that is, headers which BITS will be sending to the remote, not headers which BITS receives from the remote).

## -parameters

### -param pRequestHeaders [out]

Null-terminated string that contains the custom headers. Each header is terminated by a carriage return and line feed (CR/LF) character. To free the string when finished, call  the 
<a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a> function.

## -returns

The following table lists some of the possible return values.

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
Successfully retrieved the headers.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The job does not specify custom headers.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ACCESSDENIED</b></dt>
</dl>
</td>
<td width="60%">
Either you don't have permission to retrieve the custom headers, or [IBackgroundCopyJobHttpOptions3::MakeCustomHeadersWriteOnly](/windows/desktop/api/bits10_3/nf-bits10_3-ibackgroundcopyjobhttpoptions3-makecustomheaderswriteonly) has been called on the job.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_X_NULL_REF_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>pRequestHeaders</i> parameter is <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

Only the job owner can retrieve the custom headers. To specify the headers, call the <a href="/windows/desktop/api/bits2_5/nf-bits2_5-ibackgroundcopyjobhttpoptions-setcustomheaders">IBackgroundCopyJobHttpOptions::SetCustomHeaders</a> method.

## -see-also

<a href="/windows/desktop/api/bits2_5/nn-bits2_5-ibackgroundcopyjobhttpoptions">IBackgroundCopyJobHttpOptions</a>



<a href="/windows/desktop/api/bits2_5/nf-bits2_5-ibackgroundcopyjobhttpoptions-setcustomheaders">IBackgroundCopyJobHttpOptions::SetCustomHeaders</a>