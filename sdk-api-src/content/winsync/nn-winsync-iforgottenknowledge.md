---
UID: NN:winsync.IForgottenKnowledge
title: IForgottenKnowledge (winsync.h)
description: Represents knowledge that has been forgotten because of tombstone cleanup.
helpviewer_keywords: ["IForgottenKnowledge","IForgottenKnowledge interface [Windows Sync]","IForgottenKnowledge interface [Windows Sync]","described","winsync.iforgottenknowledge","winsync/IForgottenKnowledge"]
old-location: winsync\iforgottenknowledge.htm
tech.root: winsync
ms.assetid: 93185921-8f41-4222-86d8-602d197c4b33
ms.date: 12/05/2018
ms.keywords: IForgottenKnowledge, IForgottenKnowledge interface [Windows Sync], IForgottenKnowledge interface [Windows Sync],described, winsync.iforgottenknowledge, winsync/IForgottenKnowledge
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
 - IForgottenKnowledge
 - winsync/IForgottenKnowledge
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
 - IForgottenKnowledge
---

# IForgottenKnowledge interface


## -description

Represents knowledge that has been forgotten because of tombstone cleanup.

## -inheritance

The <b>IForgottenKnowledge</b> interface inherits from <b>ISyncKnowledge</b>. <b>IForgottenKnowledge</b> also has these types of members:

## -remarks

The forgotten knowledge tracks the maximum version of tombstones that have been cleaned up. When an item is deleted from the item store, the metadata for that item is kept, but the item is marked as deleted. Metadata for a deleted item is called a tombstone. Tombstones must be periodically cleaned up or they will eventually use too much space in the item store. When a tombstone is removed from the metadata, the forgotten knowledge must be updated to contain the version of the removed tombstone. Be aware that forgotten knowledge is an overestimation of which items have had their metadata removed. Therefore, the forgotten knowledge might also contain items that still have active entries in the metadata.

## -see-also

<b>ISyncKnowledge</b>



<a href="/previous-versions/windows/desktop/winsync/windows-sync-interfaces">Windows Sync Interfaces</a>
