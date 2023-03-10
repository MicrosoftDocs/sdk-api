---
UID: NF:bits3_0.IBackgroundCopyFile3.GetTemporaryName
title: IBackgroundCopyFile3::GetTemporaryName (bits3_0.h)
description: Gets the full path of the temporary file that contains the content of the download.
helpviewer_keywords: ["GetTemporaryName","GetTemporaryName method [BITS]","GetTemporaryName method [BITS]","IBackgroundCopyFile3 interface","IBackgroundCopyFile3 interface [BITS]","GetTemporaryName method","IBackgroundCopyFile3.GetTemporaryName","IBackgroundCopyFile3::GetTemporaryName","bits.ibackgroundcopyfile3_gettemporaryname","bits3_0/IBackgroundCopyFile3::GetTemporaryName"]
old-location: bits\ibackgroundcopyfile3_gettemporaryname.htm
tech.root: Bits
ms.assetid: 3fa4cc3b-b134-4e11-8bb6-1c9855d8dd37
ms.date: 12/05/2018
ms.keywords: GetTemporaryName, GetTemporaryName method [BITS], GetTemporaryName method [BITS],IBackgroundCopyFile3 interface, IBackgroundCopyFile3 interface [BITS],GetTemporaryName method, IBackgroundCopyFile3.GetTemporaryName, IBackgroundCopyFile3::GetTemporaryName, bits.ibackgroundcopyfile3_gettemporaryname, bits3_0/IBackgroundCopyFile3::GetTemporaryName
req.header: bits3_0.h
req.include-header: Bits.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Bits3_0.idl
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
 - IBackgroundCopyFile3::GetTemporaryName
 - bits3_0/IBackgroundCopyFile3::GetTemporaryName
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
 - IBackgroundCopyFile3.GetTemporaryName
---

# IBackgroundCopyFile3::GetTemporaryName


## -description

Gets the full path of the temporary file that contains the content of the download.

## -parameters

### -param pFilename [out]

Null-terminated string that contains the full path of the temporary file. Call the 
<a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a> function to free <i>ppFileName</i> when done.

## -returns

The method returns the following return values.

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
Success

</td>
</tr>
</table>

## -remarks

Applications can use this method to gain access to the data before the job is complete. Open the file for shared write access (FILE_SHARE_WRITE). To determine how many bytes have been transferred and are available for reading, call the <a href="/windows/desktop/api/bits/nf-bits-ibackgroundcopyfile-getprogress">IBackgroundCopyFile::GetProgress</a> method. Note that the progress information will be set back to zero if the time stamp of the URL changes.

Do not open the file for reading until BITS begins transferring the file; otherwise, the job will go into the transient error state. 

 The temporary file is available until the application calls the <a href="/windows/desktop/api/bits/nf-bits-ibackgroundcopyjob-complete">IBackgroundCopyJob::Complete</a> or <a href="/windows/desktop/api/bits/nf-bits-ibackgroundcopyjob-cancel">IBackgroundCopyJob::Cancel</a> method, or the JobInactivityTimeout group policy expires. You must release your handle to the temporary file before calling the <b>Complete</b> or <b>Cancel</b> method.

The ACL for the temporary file is the same as that of the final file when <a href="/windows/desktop/api/bits/nf-bits-ibackgroundcopyjob-complete">Complete</a> is called (the ACL is inherited from the folder). 

To determine if BITS finished transferring the file, you can:

<ul>
<li>Call the <a href="/windows/desktop/api/bits/nf-bits-ibackgroundcopyfile-getprogress">IBackgroundCopyFile::GetProgress</a> method and compare <b>BytesTransferred</b> to <b>BytesTotal</b>.</li>
<li>Implement the <a href="/windows/desktop/api/bits3_0/nf-bits3_0-ibackgroundcopycallback2-filetransferred">IBackgroundCopyCallback2::FileTransferred</a> callback.</li>
</ul>

## -see-also

<a href="/windows/desktop/api/bits3_0/nf-bits3_0-ibackgroundcopycallback2-filetransferred">IBackgroundCopyCallback2::FileTransferred</a>



<a href="/windows/desktop/api/bits3_0/nn-bits3_0-ibackgroundcopyfile3">IBackgroundCopyFile3</a>