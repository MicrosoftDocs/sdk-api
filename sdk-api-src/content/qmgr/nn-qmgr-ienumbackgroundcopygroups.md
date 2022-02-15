---
UID: NN:qmgr.IEnumBackgroundCopyGroups
title: IEnumBackgroundCopyGroups (qmgr.h)
description: Use the IEnumBackgroundCopyGroups interface to enumerate the list of groups in the download queue. To get an IEnumBackgroundCopyGroups interface pointer, call the IBackgroundCopyQMgr::EnumGroups method.
helpviewer_keywords: ["IEnumBackgroundCopyGroups","IEnumBackgroundCopyGroups interface [BITS]","IEnumBackgroundCopyGroups interface [BITS]","described","bits.ienumbackgroundcopygroups","qmgr/IEnumBackgroundCopyGroups"]
old-location: bits\ienumbackgroundcopygroups.htm
tech.root: Bits
ms.assetid: 64a05103-9749-41fd-9987-8bb17b9284f7
ms.date: 12/05/2018
ms.keywords: IEnumBackgroundCopyGroups, IEnumBackgroundCopyGroups interface [BITS], IEnumBackgroundCopyGroups interface [BITS],described, bits.ienumbackgroundcopygroups, qmgr/IEnumBackgroundCopyGroups
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
 - IEnumBackgroundCopyGroups
 - qmgr/IEnumBackgroundCopyGroups
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
 - IEnumBackgroundCopyGroups
---

# IEnumBackgroundCopyGroups interface


## -description

<p class="CCE_Message">[<b>IEnumBackgroundCopyGroups</b> is available for use in the operating systems specified in the Requirements section.  It may be altered or unavailable in subsequent versions. Instead, use the <a href="/windows/desktop/Bits/bits-interfaces">BITS interfaces</a>.]

Use the <b>IEnumBackgroundCopyGroups</b> interface to enumerate the list of groups in the download queue. To get an <b>IEnumBackgroundCopyGroups</b> interface pointer, call the <a href="/windows/desktop/api/qmgr/nf-qmgr-ibackgroundcopyqmgr-enumgroups">IBackgroundCopyQMgr::EnumGroups</a> method.

## -inheritance

The <b>IEnumBackgroundCopyGroups</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IEnumBackgroundCopyGroups</b> also has these types of members:

