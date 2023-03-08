---
UID: NN:qmgr.IEnumBackgroundCopyJobs1
title: IEnumBackgroundCopyJobs1 (qmgr.h)
description: Use the IEnumBackgroundCopyJobs1 interface to enumerate the list of jobs in a group. To get an IEnumBackgroundCopyJobs1 interface pointer, call the IBackgroundCopyGroup::EnumJobs method.
helpviewer_keywords: ["IEnumBackgroundCopyJobs1","IEnumBackgroundCopyJobs1 interface [BITS]","IEnumBackgroundCopyJobs1 interface [BITS]","described","bits.ienumbackgroundcopyjobs1","qmgr/IEnumBackgroundCopyJobs1"]
old-location: bits\ienumbackgroundcopyjobs1.htm
tech.root: Bits
ms.assetid: 93feac90-8eb8-49d8-9841-d78a2645fbcb
ms.date: 12/05/2018
ms.keywords: IEnumBackgroundCopyJobs1, IEnumBackgroundCopyJobs1 interface [BITS], IEnumBackgroundCopyJobs1 interface [BITS],described, bits.ienumbackgroundcopyjobs1, qmgr/IEnumBackgroundCopyJobs1
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
 - IEnumBackgroundCopyJobs1
 - qmgr/IEnumBackgroundCopyJobs1
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
 - IEnumBackgroundCopyJobs1
---

# IEnumBackgroundCopyJobs1 interface


## -description

<p class="CCE_Message">[<b>IEnumBackgroundCopyJobs1</b> is available for use in the operating systems specified in the Requirements section.  It may be altered or unavailable in subsequent versions. Instead, use the <a href="/windows/desktop/Bits/bits-interfaces">BITS interfaces</a>.]

Use the <b>IEnumBackgroundCopyJobs1</b> interface to enumerate the list of jobs in a group. To get an <b>IEnumBackgroundCopyJobs1</b> interface pointer, call the <a href="/windows/desktop/api/qmgr/nf-qmgr-ibackgroundcopygroup-enumjobs">IBackgroundCopyGroup::EnumJobs</a> method.

## -inheritance

The <b>IEnumBackgroundCopyJobs1</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IEnumBackgroundCopyJobs1</b> also has these types of members:

