---
UID: NF:qmgr.IEnumBackgroundCopyJobs1.Clone
title: IEnumBackgroundCopyJobs1::Clone (qmgr.h)
description: Use the Clone method to create another IEnumBackgroundCopyJobs1 enumerator that contains the same enumeration state as the current one.
helpviewer_keywords: ["Clone","Clone method [BITS]","Clone method [BITS]","IEnumBackgroundCopyJobs1 interface","IEnumBackgroundCopyJobs1 interface [BITS]","Clone method","IEnumBackgroundCopyJobs1.Clone","IEnumBackgroundCopyJobs1::Clone","bits.ienumbackgroundcopyjobs1_clone","qmgr/IEnumBackgroundCopyJobs1::Clone"]
old-location: bits\ienumbackgroundcopyjobs1_clone.htm
tech.root: Bits
ms.assetid: c26bec86-1cff-44bb-aa0c-c48b076ff993
ms.date: 12/05/2018
ms.keywords: Clone, Clone method [BITS], Clone method [BITS],IEnumBackgroundCopyJobs1 interface, IEnumBackgroundCopyJobs1 interface [BITS],Clone method, IEnumBackgroundCopyJobs1.Clone, IEnumBackgroundCopyJobs1::Clone, bits.ienumbackgroundcopyjobs1_clone, qmgr/IEnumBackgroundCopyJobs1::Clone
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
 - IEnumBackgroundCopyJobs1::Clone
 - qmgr/IEnumBackgroundCopyJobs1::Clone
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
 - IEnumBackgroundCopyJobs1.Clone
---

# IEnumBackgroundCopyJobs1::Clone


## -description

<p class="CCE_Message">[<b>IEnumBackgroundCopyJobs1</b> is available for use in the operating systems specified in the Requirements section.  It may be altered or unavailable in subsequent versions. Instead, use the <a href="/windows/desktop/Bits/bits-interfaces">BITS interfaces</a>.]

Use the <b>Clone</b> method to create another <a href="/windows/desktop/api/qmgr/nn-qmgr-ienumbackgroundcopyjobs1">IEnumBackgroundCopyJobs1</a> enumerator that contains the same enumeration state as the current one. 



Using this method, a client can record a particular point in the enumeration sequence, and then return to that point at a later time. The new enumerator supports the same interface as the original one.

## -parameters

### -param ppenum [out]

Receives the interface pointer to the enumeration object. If the method is unsuccessful, the value of this output variable is undefined. You must release <i>ppenum</i> when done.

## -returns

This method returns S_OK on success.

## -see-also

<a href="/windows/desktop/api/qmgr/nn-qmgr-ienumbackgroundcopyjobs1">IEnumBackgroundCopyJobs1</a>