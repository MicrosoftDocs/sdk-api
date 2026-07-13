---
UID: NN:winsync.IKnowledgeSyncProvider
title: IKnowledgeSyncProvider (winsync.h)
description: Represents a synchronization provider that uses knowledge to perform synchronization.
helpviewer_keywords: ["IKnowledgeSyncProvider","IKnowledgeSyncProvider interface [Windows Sync]","IKnowledgeSyncProvider interface [Windows Sync]","described","winsync.iknowledgesyncprovider","winsync/IKnowledgeSyncProvider"]
old-location: winsync\iknowledgesyncprovider.htm
tech.root: winsync
ms.assetid: 396bbf7e-7fd0-4a2e-8304-f87097cd5e50
ms.date: 12/05/2018
ms.keywords: IKnowledgeSyncProvider, IKnowledgeSyncProvider interface [Windows Sync], IKnowledgeSyncProvider interface [Windows Sync],described, winsync.iknowledgesyncprovider, winsync/IKnowledgeSyncProvider
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
 - IKnowledgeSyncProvider
 - winsync/IKnowledgeSyncProvider
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
 - IKnowledgeSyncProvider
---

# IKnowledgeSyncProvider interface


## -description

Represents a synchronization provider that uses knowledge to perform synchronization.

## -inheritance

The <b>IKnowledgeSyncProvider</b> interface inherits from <b>ISyncProvider</b>. <b>IKnowledgeSyncProvider</b> also has these types of members:

## -remarks

Typically, the first method that is called by a synchronization  session is <a href="/previous-versions/windows/desktop/api/winsync/nf-winsync-iknowledgesyncprovider-beginsession">BeginSession</a>. The last method is <a href="/previous-versions/windows/desktop/api/winsync/nf-winsync-iknowledgesyncprovider-endsession">EndSession</a>. All other <b>IKnowledgeSyncProvider</b> methods are called between these two methods.

For an overview of what a synchronization session is see the topic <a href="/previous-versions/windows/desktop/winsync/windows-sync-overview">Windows Sync Overview</a>.

## -see-also

<b>ISyncProvider</b>



<a href="/previous-versions/windows/desktop/winsync/windows-sync-interfaces">Windows Sync Interfaces</a>
