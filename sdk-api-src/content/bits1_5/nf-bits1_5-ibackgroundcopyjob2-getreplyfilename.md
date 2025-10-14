---
UID: NF:bits1_5.IBackgroundCopyJob2.GetReplyFileName
title: IBackgroundCopyJob2::GetReplyFileName
description: Retrieves the name of the file that contains the reply data from the server application. Call this method only if the job type is BG_JOB_TYPE_UPLOAD_REPLY.
helpviewer_keywords: ["GetReplyFileName","GetReplyFileName method [BITS]","GetReplyFileName method [BITS]","IBackgroundCopyJob2 interface","IBackgroundCopyJob2 interface [BITS]","GetReplyFileName method","IBackgroundCopyJob2.GetReplyFileName","IBackgroundCopyJob2::GetReplyFileName","_drz_ibackgroundcopyjob2_getreplyfilename","bits.ibackgroundcopyjob2_getreplyfilename","bits1_5/IBackgroundCopyJob2::GetReplyFileName"]
old-location: bits\ibackgroundcopyjob2_getreplyfilename.htm
tech.root: Bits
ms.assetid: 57f9245c-c1ae-4027-8e84-4926fa4861c3
ms.date: 12/05/2018
ms.keywords: GetReplyFileName, GetReplyFileName method [BITS], GetReplyFileName method [BITS],IBackgroundCopyJob2 interface, IBackgroundCopyJob2 interface [BITS],GetReplyFileName method, IBackgroundCopyJob2.GetReplyFileName, IBackgroundCopyJob2::GetReplyFileName, _drz_ibackgroundcopyjob2_getreplyfilename, bits.ibackgroundcopyjob2_getreplyfilename, bits1_5/IBackgroundCopyJob2::GetReplyFileName
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
 - IBackgroundCopyJob2::GetReplyFileName
 - bits1_5/IBackgroundCopyJob2::GetReplyFileName
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
 - IBackgroundCopyJob2.GetReplyFileName
---

# IBackgroundCopyJob2::GetReplyFileName


## -description

Retrieves the name of the file that contains the reply data from the server application. Call this method only if the job type is BG_JOB_TYPE_UPLOAD_REPLY.

## -parameters

### -param pReplyFileName [out]

Null-terminated string that contains the full path to the reply file. Call the 
<a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a> function to free <i>pReplyFileName</i> when done.

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
Successfully retrieved the name of the file that contains the reply data.

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

To specify a reply file name, call the 
<a href="/windows/desktop/api/bits1_5/nf-bits1_5-ibackgroundcopyjob2-setreplyfilename">IBackgroundCopyJob2::SetReplyFileName</a> method. If you did not specify a name, the 
<b>GetReplyFileName</b> method returns the name that BITS generated for you. If you did not specify a name and you called this method before adding a file to the job, <i>pReplyFileName</i> is set to <b>NULL</b>.

You must call the 
<a href="/windows/desktop/api/bits/nf-bits-ibackgroundcopyjob-complete">IBackgroundCopyJob::Complete</a> method before opening and reading the reply file; the reply file is not available to the client until you call the 
<b>Complete</b> method.

The file is empty if the server application did not provide a reply.


#### Examples

For an example that uses the 
<b>GetReplyFileName</b> method, see 
<a href="/windows/desktop/Bits/retrieving-the-reply-from-an-upload-reply-job">Retrieving the Reply From an Upload-Reply Job</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/bits1_5/nf-bits1_5-ibackgroundcopyjob2-getreplydata">IBackgroundCopyJob2::GetReplyData</a>



<a href="/windows/desktop/api/bits1_5/nf-bits1_5-ibackgroundcopyjob2-setreplyfilename">IBackgroundCopyJob2::SetReplyFileName</a>