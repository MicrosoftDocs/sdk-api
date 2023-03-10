---
UID: NN:winsync.IReplicaKeyMap
title: IReplicaKeyMap (winsync.h)
description: Represents a mapping between replica keys and replica IDs.
helpviewer_keywords: ["IReplicaKeyMap","IReplicaKeyMap interface [Windows Sync]","IReplicaKeyMap interface [Windows Sync]","described","winsync.ireplicakeymap","winsync/IReplicaKeyMap"]
old-location: winsync\ireplicakeymap.htm
tech.root: winsync
ms.assetid: 3c195842-316a-4c49-ace4-444fa4a38ad2
ms.date: 12/05/2018
ms.keywords: IReplicaKeyMap, IReplicaKeyMap interface [Windows Sync], IReplicaKeyMap interface [Windows Sync],described, winsync.ireplicakeymap, winsync/IReplicaKeyMap
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
 - IReplicaKeyMap
 - winsync/IReplicaKeyMap
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
 - IReplicaKeyMap
---

# IReplicaKeyMap interface


## -description

Represents a mapping between replica keys and replica IDs.

## -inheritance

The <b>IReplicaKeyMap</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IReplicaKeyMap</b> also has these types of members:

## -remarks

Because replica IDs repeatedly occur in the metadata for a replica and are suggested to be 16-byte GUIDs, Windows Sync represents replica IDs by using a map between replica IDs to 4-byte replica keys. Windows Sync then uses replica keys where references to particular replicas are required.

## -see-also

<a href="/previous-versions/windows/desktop/winsync/windows-sync-interfaces">Windows Sync Interfaces</a>
