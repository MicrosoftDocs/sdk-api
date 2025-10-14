---
UID: NF:bits1_5.IBackgroundCopyJob2.GetReplyData
title: IBackgroundCopyJob2::GetReplyData
description: Retrieves an in-memory copy of the reply data from the server application. Call this method only if the job's type is BG_JOB_TYPE_UPLOAD_REPLY and its state is BG_JOB_STATE_TRANSFERRED.
helpviewer_keywords: ["GetReplyData","GetReplyData method [BITS]","GetReplyData method [BITS]","IBackgroundCopyJob2 interface","IBackgroundCopyJob2 interface [BITS]","GetReplyData method","IBackgroundCopyJob2.GetReplyData","IBackgroundCopyJob2::GetReplyData","_drz_ibackgroundcopyjob2_getreplydata","bits.ibackgroundcopyjob2_getreplydata","bits1_5/IBackgroundCopyJob2::GetReplyData"]
old-location: bits\ibackgroundcopyjob2_getreplydata.htm
tech.root: Bits
ms.assetid: f29df35f-48c2-4837-9809-46bd04f08bfb
ms.date: 12/05/2018
ms.keywords: GetReplyData, GetReplyData method [BITS], GetReplyData method [BITS],IBackgroundCopyJob2 interface, IBackgroundCopyJob2 interface [BITS],GetReplyData method, IBackgroundCopyJob2.GetReplyData, IBackgroundCopyJob2::GetReplyData, _drz_ibackgroundcopyjob2_getreplydata, bits.ibackgroundcopyjob2_getreplydata, bits1_5/IBackgroundCopyJob2::GetReplyData
req.header: bits1_5.h
req.include-header: Bits.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2003
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Bits1_5.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Bits.lib
req.dll: BitsPrx2.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: BITS 1.5 on  Windows XP
ms.custom: 19H1
f1_keywords:
 - IBackgroundCopyJob2::GetReplyData
 - bits1_5/IBackgroundCopyJob2::GetReplyData
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - BitsPrx2.dll
api_name:
 - IBackgroundCopyJob2.GetReplyData
---

# IBackgroundCopyJob2::GetReplyData


## -description

Retrieves an in-memory copy of the reply data from the server application. Call this method only if the job's type is BG_JOB_TYPE_UPLOAD_REPLY and its state is BG_JOB_STATE_TRANSFERRED.

## -parameters

### -param ppBuffer [in, out]

Buffer to contain the reply data. The method sets <i>ppBuffer</i> to <b>NULL</b> if the server application did not return a reply. Call the 
<a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a> function to free <i>ppBuffer</i> when done.

### -param pLength [out]

Size, in bytes, of the reply data in <i>ppBuffer</i>.

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
Successfully retrieved the reply data.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>BG_E_TOO_LARGE</b></dt>
</dl>
</td>
<td width="60%">
The reply data exceeds the maximum 1 MB buffer size. The <i>ppBuffer</i> parameter is set to <b>NULL</b>, and <i>pSize</i> contains the size of the reply data.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>BG_E_INVALID_STATE</b></dt>
</dl>
</td>
<td width="60%">
To retrieve the reply data, the state of the job must be <b>BG_JOB_STATE_TRANSFERRED</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
This method is not implemented for jobs of type <b>BG_JOB_TYPE_DOWNLOAD</b> or <b>BG_JOB_TYPE_UPLOAD</b>.

</td>
</tr>
</table>

## -remarks

The 
<b>GetReplyData</b> method lets you read the reply data before or after you call the 
<a href="/windows/desktop/api/bits/nf-bits-ibackgroundcopyjob-complete">IBackgroundCopyJob::Complete</a> method. However, to read the reply data from the reply file, you must first call the 
<b>Complete</b> method; the file is not available to the client until you call the 
<b>Complete</b> method.

The 
<b>GetReplyData</b> method returns <b>BG_E_TOO_LARGE</b> if the reply data exceeds 1 MB (<i>pSize</i> contains the size of the reply data). To retrieve the reply if it exceeds 1 MB, call the 
<a href="/windows/desktop/api/bits1_5/nf-bits1_5-ibackgroundcopyjob2-getreplyfilename">IBackgroundCopyJob2::GetReplyFileName</a> method to retrieve the file name. Then, open the file and read the reply data directly.


#### Examples

For an example that uses the 
<b>GetReplyData</b> method, see 
<a href="/windows/desktop/Bits/retrieving-the-reply-from-an-upload-reply-job">Retrieving the Reply From an Upload-Reply Job</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/bits1_5/nf-bits1_5-ibackgroundcopyjob2-getreplyfilename">IBackgroundCopyJob2::GetReplyFileName</a>



<a href="/windows/desktop/api/bits1_5/nf-bits1_5-ibackgroundcopyjob2-setreplyfilename">IBackgroundCopyJob2::SetReplyFileName</a>