---
UID: NN:winsync.ISyncChangeBatchBase
title: ISyncChangeBatchBase (winsync.h)
description: Represents metadata for a set of changes. (ISyncChangeBatchBase)
helpviewer_keywords: ["ISyncChangeBatchBase","ISyncChangeBatchBase interface [Windows Sync]","ISyncChangeBatchBase interface [Windows Sync]","described","winsync.isyncchangebatchbase","winsync/ISyncChangeBatchBase"]
old-location: winsync\isyncchangebatchbase.htm
tech.root: winsync
ms.assetid: 14ca01a1-04eb-4282-adf0-e775d6ff0801
ms.date: 12/05/2018
ms.keywords: ISyncChangeBatchBase, ISyncChangeBatchBase interface [Windows Sync], ISyncChangeBatchBase interface [Windows Sync],described, winsync.isyncchangebatchbase, winsync/ISyncChangeBatchBase
req.header: winsync.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ISyncChangeBatchBase
 - winsync/ISyncChangeBatchBase
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - winsync.h
api_name:
 - ISyncChangeBatchBase
---

# ISyncChangeBatchBase interface


## -description

Represents metadata for a set of changes.

## -inheritance

The <b>ISyncChangeBatchBase</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ISyncChangeBatchBase</b> also has these types of members:

## -remarks

<b>ISyncChangeBatchBase</b> is the base interface for change batches. Typically, it is overridden by a derived interface, such as <a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-isyncchangebatch">ISyncChangeBatch</a> for a knowledge synchronization, and <a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-isyncfullenumerationchangebatch">ISyncFullEnumerationChangeBatch</a> for a full enumeration synchronization.

## -see-also

<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-ienumsyncchanges">IEnumSyncChanges Interface</a>



<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-isyncchangebatch">ISyncChangeBatch Interface</a>



<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-isyncchangebatchadvanced">ISyncChangeBatchAdvanced Interface</a>



<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-isyncchangebatchbase2">ISyncChangeBatchBase2 Interface</a>



<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-isyncchangebatchwithprerequisite">ISyncChangeBatchWithPrerequisite Interface</a>



<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-isyncfullenumerationchangebatch">ISyncFullEnumerationChangeBatch Interface</a>



<a href="/previous-versions/windows/desktop/winsync/windows-sync-interfaces">Windows Sync Interfaces</a>
