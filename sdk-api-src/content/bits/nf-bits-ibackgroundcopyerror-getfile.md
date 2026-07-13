---
UID: NF:bits.IBackgroundCopyError.GetFile
title: IBackgroundCopyError::GetFile (bits.h)
description: Retrieves an interface pointer to the file object associated with the error.
helpviewer_keywords: ["GetFile","GetFile method [BITS]","GetFile method [BITS]","IBackgroundCopyError interface","IBackgroundCopyError interface [BITS]","GetFile method","IBackgroundCopyError.GetFile","IBackgroundCopyError::GetFile","_drz_ibackgroundcopyerror_getfile","bits.ibackgroundcopyerror_getfile","bits/IBackgroundCopyError::GetFile"]
old-location: bits\ibackgroundcopyerror_getfile.htm
tech.root: Bits
ms.assetid: 7b6d4bd4-2102-4e6b-b250-1d73fae94cf9
ms.date: 12/05/2018
ms.keywords: GetFile, GetFile method [BITS], GetFile method [BITS],IBackgroundCopyError interface, IBackgroundCopyError interface [BITS],GetFile method, IBackgroundCopyError.GetFile, IBackgroundCopyError::GetFile, _drz_ibackgroundcopyerror_getfile, bits.ibackgroundcopyerror_getfile, bits/IBackgroundCopyError::GetFile
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
 - IBackgroundCopyError::GetFile
 - bits/IBackgroundCopyError::GetFile
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
 - IBackgroundCopyError.GetFile
---

# IBackgroundCopyError::GetFile


## -description

Retrieves an interface pointer to the file object associated with the error.

## -parameters

### -param pVal [out]

An <a href="/windows/desktop/api/bits/nn-bits-ibackgroundcopyfile">IBackgroundCopyFile</a> interface pointer whose methods you use to determine the local and remote file names associated with the error. The <i>ppFile</i> parameter is set to <b>NULL</b> if the error is not associated with the local or remote file. When done, release <i>ppFile</i>.

## -returns

This method returns the following <b>HRESULT</b> values.

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
Successfully retrieved an interface pointer to the file object.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>BG_E_FILE_NOT_AVAILABLE</b></dt>
</dl>
</td>
<td width="60%">
The error is not associated with a local or remote file. The <i>ppFile</i> parameter is set to <b>NULL</b>.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/bits/nf-bits-ibackgroundcopyerror-geterror">IBackgroundCopyError::GetError</a>



<a href="/windows/desktop/api/bits/nf-bits-ibackgroundcopyerror-geterrorcontextdescription">IBackgroundCopyError::GetErrorContextDescription</a>



<a href="/windows/desktop/api/bits/nf-bits-ibackgroundcopyerror-geterrordescription">IBackgroundCopyError::GetErrorDescription</a>