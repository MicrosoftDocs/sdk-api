---
UID: NF:qmgr.IBackgroundCopyJob1.AddFiles
title: IBackgroundCopyJob1::AddFiles (qmgr.h)
description: Use the AddFiles method to add one or more files to download to the job.
helpviewer_keywords: ["AddFiles","AddFiles method [BITS]","AddFiles method [BITS]","IBackgroundCopyJob1 interface","IBackgroundCopyJob1 interface [BITS]","AddFiles method","IBackgroundCopyJob1.AddFiles","IBackgroundCopyJob1::AddFiles","bits.ibackgroundcopyjob1_addfiles","qmgr/IBackgroundCopyJob1::AddFiles"]
old-location: bits\ibackgroundcopyjob1_addfiles.htm
tech.root: Bits
ms.assetid: 4a9860da-3977-4b97-957f-dd4de1e775cb
ms.date: 12/05/2018
ms.keywords: AddFiles, AddFiles method [BITS], AddFiles method [BITS],IBackgroundCopyJob1 interface, IBackgroundCopyJob1 interface [BITS],AddFiles method, IBackgroundCopyJob1.AddFiles, IBackgroundCopyJob1::AddFiles, bits.ibackgroundcopyjob1_addfiles, qmgr/IBackgroundCopyJob1::AddFiles
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
 - IBackgroundCopyJob1::AddFiles
 - qmgr/IBackgroundCopyJob1::AddFiles
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
 - IBackgroundCopyJob1.AddFiles
---

# IBackgroundCopyJob1::AddFiles


## -description

<p class="CCE_Message">[<b>IBackgroundCopyJob1</b> is available for use in the operating systems specified in the Requirements section.  It may be altered or unavailable in subsequent versions. Instead, use the <a href="/windows/desktop/Bits/bits-interfaces">BITS interfaces</a>.]

Use the <b>AddFiles</b> method to add one or more files to download to the job.

## -parameters

### -param cFileCount [in]

Number of files in <i>pFileInfo</i> to add to the job.

### -param ppFileSet [in]

Array of <a href="/windows/desktop/api/qmgr/ns-qmgr-filesetinfo">FILESETINFO</a> structures that contain the remote and local names of the files to download.

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
Files were successfully added to the job.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Local or remote file name is invalid. For example, the remote file name specifies an unsupported protocol.

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
</table>

## -see-also

<a href="/windows/desktop/api/qmgr/nn-qmgr-ibackgroundcopyjob1">IBackgroundCopyJob1</a>