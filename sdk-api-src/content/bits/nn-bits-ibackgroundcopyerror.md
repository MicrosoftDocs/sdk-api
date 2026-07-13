---
UID: NN:bits.IBackgroundCopyError
title: IBackgroundCopyError (bits.h)
description: Use the IBackgroundCopyError interface to determine the cause of an error and if the transfer process can proceed.
helpviewer_keywords: ["IBackgroundCopyError","IBackgroundCopyError interface [BITS]","IBackgroundCopyError interface [BITS]","described","_drz_ibackgroundcopyerror","bits.ibackgroundcopyerror","bits/IBackgroundCopyError"]
old-location: bits\ibackgroundcopyerror.htm
tech.root: Bits
ms.assetid: a0b9e887-84d5-4f67-a65c-6a807c50dafd
ms.date: 12/05/2018
ms.keywords: IBackgroundCopyError, IBackgroundCopyError interface [BITS], IBackgroundCopyError interface [BITS],described, _drz_ibackgroundcopyerror, bits.ibackgroundcopyerror, bits/IBackgroundCopyError
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
 - IBackgroundCopyError
 - bits/IBackgroundCopyError
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
 - IBackgroundCopyError
---

# IBackgroundCopyError interface


## -description

Use the  
<b>IBackgroundCopyError</b> interface to determine the cause of an error and if the transfer process can proceed.

BITS creates an error object only when the state of the job is BG_JOB_STATE_ERROR or BG_JOB_STATE_TRANSIENT_ERROR. BITS does not create an error object when an <b>IBackgroundCopyXXXX</b> interface method fails. The error object is available until BITS begins transferring data (the state of the job changes to BG_JOB_STATE_TRANSFERRING) for the job or until your application exits.

To get an 
<b>IBackgroundCopyError</b> object, call the 
<a href="/windows/desktop/api/bits/nf-bits-ibackgroundcopyjob-geterror">IBackgroundCopyJob::GetError</a> method.

## -inheritance

The <b>IBackgroundCopyError</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IBackgroundCopyError</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/bits/ne-bits-bg_job_state">BG_JOB_STATE</a>



<a href="/windows/desktop/api/bits/nf-bits-ibackgroundcopycallback-joberror">IBackgroundCopyCallback::JobError</a>



<a href="/windows/desktop/api/bits/nf-bits-ibackgroundcopyjob-geterror">IBackgroundCopyJob::GetError</a>



<a href="/windows/desktop/api/bits/nf-bits-ibackgroundcopyjob-getstate">IBackgroundCopyJob::GetState</a>



<a href="/windows/desktop/api/bits/nf-bits-ibackgroundcopymanager-geterrordescription">IBackgroundCopyManager::GetErrorDescription</a>
