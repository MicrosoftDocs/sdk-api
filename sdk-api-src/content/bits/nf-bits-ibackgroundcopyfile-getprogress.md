---
UID: NF:bits.IBackgroundCopyFile.GetProgress
title: IBackgroundCopyFile::GetProgress (bits.h)
description: Retrieves information on the progress of the file transfer.
helpviewer_keywords: ["GetProgress","GetProgress method [BITS]","GetProgress method [BITS]","IBackgroundCopyFile interface","IBackgroundCopyFile interface [BITS]","GetProgress method","IBackgroundCopyFile.GetProgress","IBackgroundCopyFile::GetProgress","_drz_ibackgroundcopyfile_getprogress","bits.ibackgroundcopyfile_getprogress","bits/IBackgroundCopyFile::GetProgress"]
old-location: bits\ibackgroundcopyfile_getprogress.htm
tech.root: Bits
ms.assetid: e72ec5af-7c21-48f8-b027-76a6c9e67f5e
ms.date: 12/05/2018
ms.keywords: GetProgress, GetProgress method [BITS], GetProgress method [BITS],IBackgroundCopyFile interface, IBackgroundCopyFile interface [BITS],GetProgress method, IBackgroundCopyFile.GetProgress, IBackgroundCopyFile::GetProgress, _drz_ibackgroundcopyfile_getprogress, bits.ibackgroundcopyfile_getprogress, bits/IBackgroundCopyFile::GetProgress
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
 - IBackgroundCopyFile::GetProgress
 - bits/IBackgroundCopyFile::GetProgress
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
 - IBackgroundCopyFile.GetProgress
---

# IBackgroundCopyFile::GetProgress


## -description

Retrieves information on the progress of the file transfer.

## -parameters

### -param pVal [out]

Structure whose members indicate the progress of the file transfer. For details on the type of progress information available, see the 
<a href="/windows/desktop/api/bits/ns-bits-bg_file_progress">BG_FILE_PROGRESS</a> structure.

## -returns

This method returns <b>S_OK</b> on success or one of the standard COM <b>HRESULT</b> values on error.

## -see-also

<a href="/windows/desktop/api/bits/ns-bits-bg_file_progress">BG_FILE_PROGRESS</a>



<a href="/windows/desktop/api/bits/nn-bits-ibackgroundcopyfile">IBackgroundCopyFile</a>



<a href="/windows/desktop/api/bits/nf-bits-ibackgroundcopyjob-getprogress">IBackgroundCopyJob::GetProgress</a>