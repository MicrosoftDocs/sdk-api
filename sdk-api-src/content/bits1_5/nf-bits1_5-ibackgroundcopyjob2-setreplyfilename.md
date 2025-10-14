---
UID: NF:bits1_5.IBackgroundCopyJob2.SetReplyFileName
title: IBackgroundCopyJob2::SetReplyFileName
description: Specifies the name of the file to contain the reply data from the server application. Call this method only if the job's type is BG_JOB_TYPE_UPLOAD_REPLY.
helpviewer_keywords: ["IBackgroundCopyJob2 interface [BITS]","SetReplyFileName method","IBackgroundCopyJob2.SetReplyFileName","IBackgroundCopyJob2::SetReplyFileName","SetReplyFileName","SetReplyFileName method [BITS]","SetReplyFileName method [BITS]","IBackgroundCopyJob2 interface","_drz_ibackgroundcopyjob2_setreplyfilename","bits.ibackgroundcopyjob2_setreplyfilename","bits1_5/IBackgroundCopyJob2::SetReplyFileName"]
old-location: bits\ibackgroundcopyjob2_setreplyfilename.htm
tech.root: Bits
ms.assetid: 9f8591a3-ecc2-497a-ac12-67e5862efde4
ms.date: 12/05/2018
ms.keywords: IBackgroundCopyJob2 interface [BITS],SetReplyFileName method, IBackgroundCopyJob2.SetReplyFileName, IBackgroundCopyJob2::SetReplyFileName, SetReplyFileName, SetReplyFileName method [BITS], SetReplyFileName method [BITS],IBackgroundCopyJob2 interface, _drz_ibackgroundcopyjob2_setreplyfilename, bits.ibackgroundcopyjob2_setreplyfilename, bits1_5/IBackgroundCopyJob2::SetReplyFileName
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
 - IBackgroundCopyJob2::SetReplyFileName
 - bits1_5/IBackgroundCopyJob2::SetReplyFileName
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
 - IBackgroundCopyJob2.SetReplyFileName
---

# IBackgroundCopyJob2::SetReplyFileName


## -description

Specifies the name of the file to contain the reply data from the server application. Call this method only if the job's type is <b>BG_JOB_TYPE_UPLOAD_REPLY</b>.

## -parameters

### -param ReplyFileName [in]

Null-terminated string that contains the full path to the reply file. BITS generates the file name if <i>ReplyFileNamePathSpec</i> is <b>NULL</b> or an empty string. You cannot use wildcards in the path or file name, and directories in the path must exist. The path is limited to MAX_PATH, not including the null terminator. The user must have permissions to write to the directory. BITS does not support NTFS streams. Instead of using network drives, which are session specific, use UNC paths (for example, \\server\share\path\file). Do not include the \\? prefix in the path.

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
Successfully specified the name of the file to contain the reply data.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>BG_E_INVALID_STATE</b></dt>
</dl>
</td>
<td width="60%">
You cannot change the reply file name after BITS begins transferring the reply to the client. BITS is transferring the reply to the client if the state is <b>BG_JOB_STATE_TRANSFERRING</b> and the <b>BytesTotal</b> member of the 
<a href="/windows/desktop/api/bits1_5/ns-bits1_5-bg_job_reply_progress">BG_JOB_REPLY_PROGRESS</a> structure is not <b>BG_SIZE_UNKNOWN</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ACCESSDENIED</b></dt>
</dl>
</td>
<td width="60%">
User does not have permission to write to the specified directory on the client.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The reply file name is invalid or exceeds <b>MAX_PATH</b>.

</td>
</tr>
</table>

## -remarks

BITS generates the file name if you do not call the 
<b>SetReplyFileName</b> method before calling the 
<a href="/windows/desktop/api/bits/nf-bits-ibackgroundcopyjob-resume">IBackgroundCopyJob::Resume</a> method for the first time.

If BITS generates the file name, the reply file is written to the same directory as the local upload file.

You can call the 
<b>SetReplyFileName</b> method anytime before BITS begins downloading the reply from the server application; the method fails if the download has begun.

The reply file is available to the client after calling the 
<a href="/windows/desktop/api/bits/nf-bits-ibackgroundcopyjob-complete">IBackgroundCopyJob::Complete</a> method. To retrieve the reply data before calling the 
<b>Complete</b> method, call the 
<a href="/windows/desktop/api/bits1_5/nf-bits1_5-ibackgroundcopyjob2-getreplydata">IBackgroundCopyJob2::GetReplyData</a> method.

The file is empty if the server application did not provide a reply.

## -see-also

<a href="/windows/desktop/api/bits1_5/nf-bits1_5-ibackgroundcopyjob2-getreplydata">IBackgroundCopyJob::GetReplyData</a>



<a href="/windows/desktop/api/bits1_5/nf-bits1_5-ibackgroundcopyjob2-getreplyfilename">IBackgroundCopyJob::GetReplyFileName</a>