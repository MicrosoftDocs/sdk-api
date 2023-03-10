---
UID: NN:winsync.ISyncFullEnumerationChange
title: ISyncFullEnumerationChange (winsync.h)
description: Represents additional information about an ISyncChange object during recovery synchronization.
helpviewer_keywords: ["ISyncFullEnumerationChange","ISyncFullEnumerationChange interface [Windows Sync]","ISyncFullEnumerationChange interface [Windows Sync]","described","winsync.isyncfullenumerationchange","winsync/ISyncFullEnumerationChange"]
old-location: winsync\isyncfullenumerationchange.htm
tech.root: winsync
ms.assetid: 1e666737-c5dc-4394-9f41-6e77832dd9f6
ms.date: 12/05/2018
ms.keywords: ISyncFullEnumerationChange, ISyncFullEnumerationChange interface [Windows Sync], ISyncFullEnumerationChange interface [Windows Sync],described, winsync.isyncfullenumerationchange, winsync/ISyncFullEnumerationChange
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
 - ISyncFullEnumerationChange
 - winsync/ISyncFullEnumerationChange
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
 - ISyncFullEnumerationChange
---

# ISyncFullEnumerationChange interface


## -description

Represents additional information about an <b>ISyncChange</b> object during recovery synchronization.

## -inheritance

The <b>ISyncFullEnumerationChange</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ISyncFullEnumerationChange</b> also has these types of members:

## -remarks

To obtain an <b>ISyncFullEnumerationChange</b> object, pass <b>IID_ISyncFullEnumerationChange</b> to the <b>QueryInterface</b> method of an <a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-isyncchange">ISyncChange</a> object during recovery synchronization.

## -see-also

<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-isyncchange">ISyncChange Interface</a>



<a href="/previous-versions/windows/desktop/winsync/windows-sync-interfaces">Windows Sync Interfaces</a>
