---
UID: NN:winsync.ISyncChangeBatchAdvanced
title: ISyncChangeBatchAdvanced (winsync.h)
description: Represents additional information about a set of changes.
helpviewer_keywords: ["ISyncChangeBatchAdvanced","ISyncChangeBatchAdvanced interface [Windows Sync]","ISyncChangeBatchAdvanced interface [Windows Sync]","described","winsync.isyncchangebatchadvanced","winsync/ISyncChangeBatchAdvanced"]
old-location: winsync\isyncchangebatchadvanced.htm
tech.root: winsync
ms.assetid: b78bc885-ed4e-4c83-ad1b-043c5b226337
ms.date: 12/05/2018
ms.keywords: ISyncChangeBatchAdvanced, ISyncChangeBatchAdvanced interface [Windows Sync], ISyncChangeBatchAdvanced interface [Windows Sync],described, winsync.isyncchangebatchadvanced, winsync/ISyncChangeBatchAdvanced
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
 - ISyncChangeBatchAdvanced
 - winsync/ISyncChangeBatchAdvanced
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
 - ISyncChangeBatchAdvanced
---

# ISyncChangeBatchAdvanced interface


## -description

Represents additional information about a set of changes.

## -inheritance

The <b>ISyncChangeBatchAdvanced</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ISyncChangeBatchAdvanced</b> also has these types of members:

## -remarks

An <b>ISyncChangeBatchAdvanced</b> object can be obtained by passing <b>IID_ISyncChangeBatchAdvanced</b> to the <b>QueryInterface</b> method of a change batch object, such as an <a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-isyncchangebatch">ISyncChangeBatch</a> or <a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-isyncfullenumerationchangebatch">ISyncFullEnumerationChangeBatch</a> object.

## -see-also

<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-isyncchangebatch">ISyncChangeBatch Interface</a>



<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-isyncchangebatchbase">ISyncChangeBatchBase Interface</a>



<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-isyncchangebatchbase2">ISyncChangeBatchBase2 Interface</a>



<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-isyncchangebatchwithprerequisite">ISyncChangeBatchWithPrerequisite Interface</a>



<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-isyncfilterinfo">ISyncFilterInfo Interface</a>



<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-isyncfullenumerationchangebatch">ISyncFullEnumerationChangeBatch Interface</a>



<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-isyncknowledge">ISyncKnowledge Interface</a>



<a href="/previous-versions/windows/desktop/winsync/windows-sync-interfaces">Windows Sync Interfaces</a>
