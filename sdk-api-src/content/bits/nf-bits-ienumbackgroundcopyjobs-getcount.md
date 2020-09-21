---
UID: NF:bits.IEnumBackgroundCopyJobs.GetCount
title: IEnumBackgroundCopyJobs::GetCount (bits.h)
description: Retrieves a count of the number of jobs in the enumeration.
helpviewer_keywords: ["GetCount","GetCount method [BITS]","GetCount method [BITS]","IEnumBackgroundCopyJobs interface","IEnumBackgroundCopyJobs interface [BITS]","GetCount method","IEnumBackgroundCopyJobs.GetCount","IEnumBackgroundCopyJobs::GetCount","_drz_ienumbackgroundcopyjobs_getcount","bits.ienumbackgroundcopyjobs_getcount","bits/IEnumBackgroundCopyJobs::GetCount"]
old-location: bits\ienumbackgroundcopyjobs_getcount.htm
tech.root: Bits
ms.assetid: 024ffd11-5084-4ff5-b1b6-9aec3e802900
ms.date: 12/05/2018
ms.keywords: GetCount, GetCount method [BITS], GetCount method [BITS],IEnumBackgroundCopyJobs interface, IEnumBackgroundCopyJobs interface [BITS],GetCount method, IEnumBackgroundCopyJobs.GetCount, IEnumBackgroundCopyJobs::GetCount, _drz_ienumbackgroundcopyjobs_getcount, bits.ienumbackgroundcopyjobs_getcount, bits/IEnumBackgroundCopyJobs::GetCount
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
 - IEnumBackgroundCopyJobs::GetCount
 - bits/IEnumBackgroundCopyJobs::GetCount
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
 - IEnumBackgroundCopyJobs.GetCount
---

# IEnumBackgroundCopyJobs::GetCount


## -description

Retrieves a count of the number of jobs in the enumeration.

## -parameters

### -param puCount [out]

Number of jobs in the enumeration.

## -returns

This method returns <b>S_OK</b> on success or one of the standard COM <b>HRESULT</b> values on error.

## -see-also

<a href="/windows/desktop/api/bits/nn-bits-ienumbackgroundcopyjobs">IEnumBackgroundCopyJobs</a>