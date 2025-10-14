---
UID: NF:qmgr.IBackgroundCopyJob1.GetFile
title: IBackgroundCopyJob1::GetFile (qmgr.h)
description: Use the GetFile method to retrieve the remote and local file names for the given file in the job.
helpviewer_keywords: ["GetFile","GetFile method [BITS]","GetFile method [BITS]","IBackgroundCopyJob1 interface","IBackgroundCopyJob1 interface [BITS]","GetFile method","IBackgroundCopyJob1.GetFile","IBackgroundCopyJob1::GetFile","bits.ibackgroundcopyjob1_getfile","qmgr/IBackgroundCopyJob1::GetFile"]
old-location: bits\ibackgroundcopyjob1_getfile.htm
tech.root: Bits
ms.assetid: 6cd680cc-abe0-44e1-a650-079295a8dd4a
ms.date: 12/05/2018
ms.keywords: GetFile, GetFile method [BITS], GetFile method [BITS],IBackgroundCopyJob1 interface, IBackgroundCopyJob1 interface [BITS],GetFile method, IBackgroundCopyJob1.GetFile, IBackgroundCopyJob1::GetFile, bits.ibackgroundcopyjob1_getfile, qmgr/IBackgroundCopyJob1::GetFile
req.header: qmgr.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP
req.target-min-winversvr: Windows Server 2003
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Qmgr.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: QmgrPrxy.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IBackgroundCopyJob1::GetFile
 - qmgr/IBackgroundCopyJob1::GetFile
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
 - IBackgroundCopyJob1.GetFile
---

# IBackgroundCopyJob1::GetFile


## -description

<p class="CCE_Message">[<b>IBackgroundCopyJob1</b> is available for use in the operating systems specified in the Requirements section.  It may be altered or unavailable in subsequent versions. Instead, use the <a href="/windows/desktop/Bits/bits-interfaces">BITS interfaces</a>.]

Use the <b>GetFile</b> method to retrieve the remote and local file names for the given file in the job.

## -parameters

### -param cFileIndex [in]

Zero-based index that identifies the file in the job.

### -param pFileInfo [out]

A <a href="/windows/desktop/api/qmgr/ns-qmgr-filesetinfo">FILESETINFO</a> structure that contains the remote and local names of the file.

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
Successfully retrieved the file from the job.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>QM_E_ITEM_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The specified index is greater than the number of files in the job.

</td>
</tr>
</table>

## -remarks

Use with <a href="/windows/desktop/api/qmgr/nf-qmgr-ibackgroundcopyjob1-getfilecount">IBackgroundCopyJob1::GetFileCount</a> to iterate through the files of a job.

## -see-also

<a href="/windows/desktop/api/qmgr/nn-qmgr-ibackgroundcopyjob1">IBackgroundCopyJob1</a>