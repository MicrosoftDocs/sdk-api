---
UID: NF:bits.IEnumBackgroundCopyJobs.Clone
title: IEnumBackgroundCopyJobs::Clone (bits.h)
description: Creates another IEnumBackgroundCopyJobs enumerator that contains the same enumeration state as the current one.
helpviewer_keywords: ["Clone","Clone method [BITS]","Clone method [BITS]","IEnumBackgroundCopyJobs interface","IEnumBackgroundCopyJobs interface [BITS]","Clone method","IEnumBackgroundCopyJobs.Clone","IEnumBackgroundCopyJobs::Clone","_drz_ienumbackgroundcopyjobs_clone","bits.ienumbackgroundcopyjobs_clone","bits/IEnumBackgroundCopyJobs::Clone"]
old-location: bits\ienumbackgroundcopyjobs_clone.htm
tech.root: Bits
ms.assetid: 5d83af74-c24c-41e2-aef4-d7210a1d0160
ms.date: 12/05/2018
ms.keywords: Clone, Clone method [BITS], Clone method [BITS],IEnumBackgroundCopyJobs interface, IEnumBackgroundCopyJobs interface [BITS],Clone method, IEnumBackgroundCopyJobs.Clone, IEnumBackgroundCopyJobs::Clone, _drz_ienumbackgroundcopyjobs_clone, bits.ienumbackgroundcopyjobs_clone, bits/IEnumBackgroundCopyJobs::Clone
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
 - IEnumBackgroundCopyJobs::Clone
 - bits/IEnumBackgroundCopyJobs::Clone
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
 - IEnumBackgroundCopyJobs.Clone
---

# IEnumBackgroundCopyJobs::Clone


## -description

Creates another 
<a href="/windows/desktop/api/bits/nn-bits-ienumbackgroundcopyjobs">IEnumBackgroundCopyJobs</a> enumerator that contains the same enumeration state as the current one.

Using this method, a client can record a particular point in the enumeration sequence, and then return to that point at a later time. The new enumerator supports the same interface as the original one.

## -parameters

### -param ppenum [out]

Receives the interface pointer to the enumeration object. If the method is unsuccessful, the value of this output variable is undefined. You must release <i>ppEnumJobs</i> when done.

## -returns

This method returns <b>S_OK</b> on success or one of the standard COM <b>HRESULT</b> values on error.

## -see-also

<a href="/windows/desktop/api/bits/nn-bits-ienumbackgroundcopyjobs">IEnumBackgroundCopyJobs</a>