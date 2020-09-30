---
UID: NF:bits.IBackgroundCopyJob.GetId
title: IBackgroundCopyJob::GetId (bits.h)
description: Retrieves the identifier used to identify the job in the queue.
helpviewer_keywords: ["GetId","GetId method [BITS]","GetId method [BITS]","IBackgroundCopyJob interface","IBackgroundCopyJob interface [BITS]","GetId method","IBackgroundCopyJob.GetId","IBackgroundCopyJob::GetId","_drz_ibackgroundcopyjob_getid","bits.ibackgroundcopyjob_getid","bits/IBackgroundCopyJob::GetId"]
old-location: bits\ibackgroundcopyjob_getid.htm
tech.root: Bits
ms.assetid: bc214b2e-fbf3-446e-abce-56e515dcfadf
ms.date: 12/05/2018
ms.keywords: GetId, GetId method [BITS], GetId method [BITS],IBackgroundCopyJob interface, IBackgroundCopyJob interface [BITS],GetId method, IBackgroundCopyJob.GetId, IBackgroundCopyJob::GetId, _drz_ibackgroundcopyjob_getid, bits.ibackgroundcopyjob_getid, bits/IBackgroundCopyJob::GetId
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
 - IBackgroundCopyJob::GetId
 - bits/IBackgroundCopyJob::GetId
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
 - IBackgroundCopyJob.GetId
---

# IBackgroundCopyJob::GetId


## -description

Retrieves the identifier used to identify the job in the queue.

## -parameters

### -param pVal [out]

GUID that identifies the job within the BITS queue.

## -returns

This method returns <b>S_OK</b> on success or one of the standard COM <b>HRESULT</b> values on error.

## -remarks

The service generates the identifier when you 
<a href="/windows/desktop/api/bits/nf-bits-ibackgroundcopymanager-createjob">create</a> the job. To use the identifier to retrieve an 
<a href="/windows/desktop/api/bits/nn-bits-ibackgroundcopyjob">IBackgroundCopyJob</a> interface pointer for the job, call the 
<a href="/windows/desktop/api/bits/nf-bits-ibackgroundcopymanager-getjob">IBackgroundCopyManager::GetJob</a> method.

## -see-also

<a href="/windows/desktop/api/bits/nf-bits-ibackgroundcopymanager-createjob">IBackgroundCopyManager::CreateJob</a>



<a href="/windows/desktop/api/bits/nf-bits-ibackgroundcopymanager-getjob">IBackgroundCopyManager::GetJob</a>