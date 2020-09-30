---
UID: NF:qmgr.IEnumBackgroundCopyJobs1.GetCount
title: IEnumBackgroundCopyJobs1::GetCount (qmgr.h)
description: Use the GetCount method to retrieve a count of the number of jobs in the enumeration.
helpviewer_keywords: ["GetCount","GetCount method [BITS]","GetCount method [BITS]","IEnumBackgroundCopyJobs1 interface","IEnumBackgroundCopyJobs1 interface [BITS]","GetCount method","IEnumBackgroundCopyJobs1.GetCount","IEnumBackgroundCopyJobs1::GetCount","bits.ienumbackgroundcopyjobs1_getcount","qmgr/IEnumBackgroundCopyJobs1::GetCount"]
old-location: bits\ienumbackgroundcopyjobs1_getcount.htm
tech.root: Bits
ms.assetid: 3deaf2fd-84a0-49f8-8a7d-91a39701683a
ms.date: 12/05/2018
ms.keywords: GetCount, GetCount method [BITS], GetCount method [BITS],IEnumBackgroundCopyJobs1 interface, IEnumBackgroundCopyJobs1 interface [BITS],GetCount method, IEnumBackgroundCopyJobs1.GetCount, IEnumBackgroundCopyJobs1::GetCount, bits.ienumbackgroundcopyjobs1_getcount, qmgr/IEnumBackgroundCopyJobs1::GetCount
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
 - IEnumBackgroundCopyJobs1::GetCount
 - qmgr/IEnumBackgroundCopyJobs1::GetCount
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
 - IEnumBackgroundCopyJobs1.GetCount
---

# IEnumBackgroundCopyJobs1::GetCount


## -description

<p class="CCE_Message">[<b>IEnumBackgroundCopyJobs1</b> is available for use in the operating systems specified in the Requirements section.  It may be altered or unavailable in subsequent versions. Instead, use the <a href="/windows/desktop/Bits/bits-interfaces">BITS interfaces</a>.]

Use the <b>GetCount</b> method to retrieve a count of the number of jobs in the enumeration.

## -parameters

### -param puCount [out]

Number of jobs in the enumeration.

## -returns

This method returns <b>S_OK</b> on success.

## -see-also

<a href="/windows/desktop/api/qmgr/nn-qmgr-ienumbackgroundcopyjobs1">IEnumBackgroundCopyJobs1</a>