---
UID: NN:bits.IBackgroundCopyJob
title: IBackgroundCopyJob (bits.h)
description: Use the IBackgroundCopyJob interface to add files to the job, set the priority level of the job, determine the state of the job, and to start and stop the job.
helpviewer_keywords: ["IBackgroundCopyJob","IBackgroundCopyJob interface [BITS]","IBackgroundCopyJob interface [BITS]","described","_drz_ibackgroundcopyjob","bits.ibackgroundcopyjob","bits/IBackgroundCopyJob"]
old-location: bits\ibackgroundcopyjob.htm
tech.root: Bits
ms.assetid: 91dd1ae1-1740-4d95-a476-fc18aead1dc2
ms.date: 12/05/2018
ms.keywords: IBackgroundCopyJob, IBackgroundCopyJob interface [BITS], IBackgroundCopyJob interface [BITS],described, _drz_ibackgroundcopyjob, bits.ibackgroundcopyjob, bits/IBackgroundCopyJob
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
 - IBackgroundCopyJob
 - bits/IBackgroundCopyJob
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
 - IBackgroundCopyJob
---

# IBackgroundCopyJob interface


## -description

Use the 
<b>IBackgroundCopyJob</b> interface to add files to the job, set the priority level of the job, determine the state of the job, and to start and stop the job.

To create a job, call the 
<a href="/windows/desktop/api/bits/nf-bits-ibackgroundcopymanager-createjob">IBackgroundCopyManager::CreateJob</a> method. To get an 
<b>IBackgroundCopyJob</b> interface pointer to an existing job, call the 
<a href="/windows/desktop/api/bits/nf-bits-ibackgroundcopymanager-getjob">IBackgroundCopyManager::GetJob</a> method.

## -inheritance

The <b>IBackgroundCopyJob</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IBackgroundCopyJob</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/bits/nn-bits-ibackgroundcopyfile">IBackgroundCopyFile</a>



<a href="/windows/desktop/api/bits1_5/nn-bits1_5-ibackgroundcopyjob2">IBackgroundCopyJob2</a>



<a href="/windows/desktop/api/bits2_0/nn-bits2_0-ibackgroundcopyjob3">IBackgroundCopyJob3</a>



<a href="/windows/desktop/api/bits/nn-bits-ibackgroundcopymanager">IBackgroundCopyManager</a>



<a href="/windows/desktop/api/bits/nn-bits-ienumbackgroundcopyjobs">IEnumBackgroundCopyJobs</a>
