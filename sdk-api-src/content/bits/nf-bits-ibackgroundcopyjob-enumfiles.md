---
UID: NF:bits.IBackgroundCopyJob.EnumFiles
title: IBackgroundCopyJob::EnumFiles (bits.h)
description: Retrieves an IEnumBackgroundCopyFiles interface pointer that you use to enumerate the files in a job.
helpviewer_keywords: ["EnumFiles","EnumFiles method [BITS]","EnumFiles method [BITS]","IBackgroundCopyJob interface","IBackgroundCopyJob interface [BITS]","EnumFiles method","IBackgroundCopyJob.EnumFiles","IBackgroundCopyJob::EnumFiles","_drz_ibackgroundcopyjob_enumfiles","bits.ibackgroundcopyjob_enumfiles","bits/IBackgroundCopyJob::EnumFiles"]
old-location: bits\ibackgroundcopyjob_enumfiles.htm
tech.root: Bits
ms.assetid: c6b8ef69-9c67-447f-9f90-b6905a5a5a19
ms.date: 12/05/2018
ms.keywords: EnumFiles, EnumFiles method [BITS], EnumFiles method [BITS],IBackgroundCopyJob interface, IBackgroundCopyJob interface [BITS],EnumFiles method, IBackgroundCopyJob.EnumFiles, IBackgroundCopyJob::EnumFiles, _drz_ibackgroundcopyjob_enumfiles, bits.ibackgroundcopyjob_enumfiles, bits/IBackgroundCopyJob::EnumFiles
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
 - IBackgroundCopyJob::EnumFiles
 - bits/IBackgroundCopyJob::EnumFiles
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
 - IBackgroundCopyJob.EnumFiles
---

# IBackgroundCopyJob::EnumFiles


## -description

Retrieves an 
<a href="/windows/desktop/api/bits/nn-bits-ienumbackgroundcopyfiles">IEnumBackgroundCopyFiles</a> interface pointer that you use to 
<a href="/windows/desktop/Bits/enumerating-files-in-a-job">enumerate the files</a> in a job.

## -parameters

### -param pEnum [out]

<a href="/windows/desktop/api/bits/nn-bits-ienumbackgroundcopyfiles">IEnumBackgroundCopyFiles</a> interface pointer that you use to enumerate the files in the job. Release <i>ppEnumFiles</i> when done.

## -returns

This method returns <b>S_OK</b> on success or one of the standard COM <b>HRESULT</b> values on error.

## -see-also

<a href="/windows/desktop/api/bits/nf-bits-ibackgroundcopymanager-enumjobs">IBackgroundCopyManager::EnumJobs</a>



<a href="/windows/desktop/api/bits/nn-bits-ienumbackgroundcopyfiles">IEnumBackgroundCopyFiles</a>