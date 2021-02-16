---
UID: NF:bits.IBackgroundCopyFile.GetRemoteName
title: IBackgroundCopyFile::GetRemoteName (bits.h)
description: Retrieves the remote name of the file.
helpviewer_keywords: ["GetRemoteName","GetRemoteName method [BITS]","GetRemoteName method [BITS]","IBackgroundCopyFile interface","IBackgroundCopyFile interface [BITS]","GetRemoteName method","IBackgroundCopyFile.GetRemoteName","IBackgroundCopyFile::GetRemoteName","_drz_ibackgroundcopyfile_getremotename","bits.ibackgroundcopyfile_getremotename","bits/IBackgroundCopyFile::GetRemoteName"]
old-location: bits\ibackgroundcopyfile_getremotename.htm
tech.root: Bits
ms.assetid: b6b1b1dc-776e-4369-bd39-d159e4edfe38
ms.date: 12/05/2018
ms.keywords: GetRemoteName, GetRemoteName method [BITS], GetRemoteName method [BITS],IBackgroundCopyFile interface, IBackgroundCopyFile interface [BITS],GetRemoteName method, IBackgroundCopyFile.GetRemoteName, IBackgroundCopyFile::GetRemoteName, _drz_ibackgroundcopyfile_getremotename, bits.ibackgroundcopyfile_getremotename, bits/IBackgroundCopyFile::GetRemoteName
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
 - IBackgroundCopyFile::GetRemoteName
 - bits/IBackgroundCopyFile::GetRemoteName
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
 - IBackgroundCopyFile.GetRemoteName
---

# IBackgroundCopyFile::GetRemoteName


## -description

Retrieves the remote name of the file.

## -parameters

### -param pVal [out]

Null-terminated string that contains the remote name of the file to transfer. The name is fully qualified. Call the 
<a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a> function to free <i>ppName</i> when done.

## -returns

This method returns <b>S_OK</b> on success or one of the standard COM <b>HRESULT</b> values on error.

## -remarks

The remote file name is set when you call the 
<a href="/windows/desktop/api/bits/nf-bits-ibackgroundcopyjob-addfile">AddFile</a> or 
<a href="/windows/desktop/api/bits/nf-bits-ibackgroundcopyjob-addfileset">AddFileSet</a> methods of the 
<a href="/windows/desktop/api/bits/nn-bits-ibackgroundcopyjob">IBackgroundCopyJob</a> interface.

To change the remote file name, call the <a href="/windows/desktop/api/bits2_0/nf-bits2_0-ibackgroundcopyfile2-setremotename">IBackgroundCopyFile2::SetRemoteName</a> method or the <a href="/windows/desktop/api/bits2_0/nf-bits2_0-ibackgroundcopyjob3-replaceremoteprefix">IBackgroundCopyJob3::ReplaceRemotePrefix</a> method.


#### Examples

See the example code for the 
<a href="/windows/desktop/api/bits/nf-bits-ibackgroundcopyfile-getlocalname">IBackgroundCopyFile::GetLocalName</a> method.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/bits/nn-bits-ibackgroundcopyfile">IBackgroundCopyFile</a>



<a href="/windows/desktop/api/bits/nf-bits-ibackgroundcopyfile-getlocalname">IBackgroundCopyFile::GetLocalName</a>



<a href="/windows/desktop/api/bits/nf-bits-ibackgroundcopyjob-addfile">IBackgroundCopyJob::AddFile</a>



<a href="/windows/desktop/api/bits/nf-bits-ibackgroundcopyjob-addfileset">IBackgroundCopyJob::AddFileSet</a>