---
UID: NN:winsync.ISyncChangeBatch
title: ISyncChangeBatch (winsync.h)
description: Represents metadata for a set of changes. (ISyncChangeBatch)
helpviewer_keywords: ["ISyncChangeBatch","ISyncChangeBatch interface [Windows Sync]","ISyncChangeBatch interface [Windows Sync]","described","winsync.isyncchangebatch","winsync/ISyncChangeBatch"]
old-location: winsync\isyncchangebatch.htm
tech.root: winsync
ms.assetid: 3bfd5cf2-ca73-490e-84a7-506c198b3d7c
ms.date: 12/05/2018
ms.keywords: ISyncChangeBatch, ISyncChangeBatch interface [Windows Sync], ISyncChangeBatch interface [Windows Sync],described, winsync.isyncchangebatch, winsync/ISyncChangeBatch
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
 - ISyncChangeBatch
 - winsync/ISyncChangeBatch
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
 - ISyncChangeBatch
---

# ISyncChangeBatch interface


## -description

Represents metadata for a set of changes.

## -inheritance

The <b>ISyncChangeBatch</b> interface inherits from <b>ISyncChangeBatchBase</b>. <b>ISyncChangeBatch</b> also has these types of members:

## -remarks

Change batches are used by synchronization providers to communicate metadata for item changes from a source provider to a destination provider. The source provider enumerates changes and adds a specified number of them to a change batch. The change batch is then sent to the destination provider. The destination provider enumerates the changes in the change batch and applies them to its item store.

## -see-also

<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-isyncchangebatchadvanced">ISyncChangeBatchAdvanced Interface</a>



<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-isyncchangebatchbase">ISyncChangeBatchBase Interface</a>



<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-isyncchangebatchbase2">ISyncChangeBatchBase2 Interface</a>



<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-isyncchangebatchwithprerequisite">ISyncChangeBatchWithPrerequisite Interface</a>



<a href="/previous-versions/windows/desktop/winsync/windows-sync-interfaces">Windows Sync Interfaces</a>
