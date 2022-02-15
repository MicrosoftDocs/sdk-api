---
UID: NN:bits.IEnumBackgroundCopyJobs
title: IEnumBackgroundCopyJobs (bits.h)
description: Use the IEnumBackgroundCopyJobs interface to enumerate the list of jobs in the transfer queue. To get an IEnumBackgroundCopyJobs interface pointer, call the IBackgroundCopyManager::EnumJobs method.
helpviewer_keywords: ["IEnumBackgroundCopyJobs","IEnumBackgroundCopyJobs interface [BITS]","IEnumBackgroundCopyJobs interface [BITS]","described","_drz_ienumbackgroundcopyjobs","bits.ienumbackgroundcopyjobs","bits/IEnumBackgroundCopyJobs"]
old-location: bits\ienumbackgroundcopyjobs.htm
tech.root: Bits
ms.assetid: 21ff88da-9fae-478f-bcba-488ed7a89608
ms.date: 12/05/2018
ms.keywords: IEnumBackgroundCopyJobs, IEnumBackgroundCopyJobs interface [BITS], IEnumBackgroundCopyJobs interface [BITS],described, _drz_ienumbackgroundcopyjobs, bits.ienumbackgroundcopyjobs, bits/IEnumBackgroundCopyJobs
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
 - IEnumBackgroundCopyJobs
 - bits/IEnumBackgroundCopyJobs
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
 - IEnumBackgroundCopyJobs
---

# IEnumBackgroundCopyJobs interface


## -description

Use the 
<b>IEnumBackgroundCopyJobs</b> interface to enumerate the list of jobs in the transfer queue. To get an 
<b>IEnumBackgroundCopyJobs</b> interface pointer, call the 
<a href="/windows/desktop/api/bits/nf-bits-ibackgroundcopymanager-enumjobs">IBackgroundCopyManager::EnumJobs</a> method.

## -inheritance

The <b>IEnumBackgroundCopyJobs</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IEnumBackgroundCopyJobs</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/bits/nf-bits-ibackgroundcopymanager-enumjobs">IBackgroundCopyManager::EnumJobs</a>



<a href="/windows/desktop/api/bits/nn-bits-ienumbackgroundcopyfiles">IEnumBackgroundCopyFiles</a>
