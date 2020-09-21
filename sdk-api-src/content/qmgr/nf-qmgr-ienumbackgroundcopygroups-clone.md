---
UID: NF:qmgr.IEnumBackgroundCopyGroups.Clone
title: IEnumBackgroundCopyGroups::Clone (qmgr.h)
description: Use the Clone method to create another IEnumBackgroundCopyGroups enumerator that contains the same enumeration state as the current one.
helpviewer_keywords: ["Clone","Clone method [BITS]","Clone method [BITS]","IEnumBackgroundCopyGroups interface","IEnumBackgroundCopyGroups interface [BITS]","Clone method","IEnumBackgroundCopyGroups.Clone","IEnumBackgroundCopyGroups::Clone","bits.ienumbackgroundcopygroups_clone","qmgr/IEnumBackgroundCopyGroups::Clone"]
old-location: bits\ienumbackgroundcopygroups_clone.htm
tech.root: Bits
ms.assetid: f2743edd-9fc5-451b-b1ff-17f4591923ba
ms.date: 12/05/2018
ms.keywords: Clone, Clone method [BITS], Clone method [BITS],IEnumBackgroundCopyGroups interface, IEnumBackgroundCopyGroups interface [BITS],Clone method, IEnumBackgroundCopyGroups.Clone, IEnumBackgroundCopyGroups::Clone, bits.ienumbackgroundcopygroups_clone, qmgr/IEnumBackgroundCopyGroups::Clone
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
 - IEnumBackgroundCopyGroups::Clone
 - qmgr/IEnumBackgroundCopyGroups::Clone
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
 - IEnumBackgroundCopyGroups.Clone
---

# IEnumBackgroundCopyGroups::Clone


## -description

<p class="CCE_Message">[<b>IEnumBackgroundCopyGroups</b> is available for use in the operating systems specified in the Requirements section.  It may be altered or unavailable in subsequent versions. Instead, use the <a href="/windows/desktop/Bits/bits-interfaces">BITS interfaces</a>.]

Use the <b>Clone</b> method to create another <a href="/windows/desktop/api/qmgr/nn-qmgr-ienumbackgroundcopygroups">IEnumBackgroundCopyGroups</a> enumerator that contains the same enumeration state as the current one. 



Using this method, a client can record a particular point in the enumeration sequence, and then return to that point at a later time. The new enumerator supports the same interface as the original one.

## -parameters

### -param ppenum [out]

Receives the interface pointer to the enumeration object. If the method is unsuccessful, the value of this output variable is undefined. You must release <i>ppenum</i> when done.

## -returns

This method returns <b>S_OK</b> on success.

## -see-also

<a href="/windows/desktop/api/qmgr/nn-qmgr-ienumbackgroundcopygroups">IEnumBackgroundCopyGroups</a>