---
UID: NN:syncmgr.ISyncMgrSyncItem
title: ISyncMgrSyncItem (syncmgr.h)
description: Exposes methods that act on and retrieve information from a single sync item, allowing handlers to manage sync items as independent objects.
helpviewer_keywords: ["ISyncMgrSyncItem","ISyncMgrSyncItem interface [Windows Shell]","ISyncMgrSyncItem interface [Windows Shell]","described","_shell_ISyncMgrSyncItem","shell.ISyncMgrSyncItem","syncmgr/ISyncMgrSyncItem"]
old-location: shell\ISyncMgrSyncItem.htm
tech.root: shell
ms.assetid: 322c2ebe-f1ab-4de4-b8d5-2fba1e69ddda
ms.date: 12/05/2018
ms.keywords: ISyncMgrSyncItem, ISyncMgrSyncItem interface [Windows Shell], ISyncMgrSyncItem interface [Windows Shell],described, _shell_ISyncMgrSyncItem, shell.ISyncMgrSyncItem, syncmgr/ISyncMgrSyncItem
req.header: syncmgr.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Syncmgr.idl
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
 - ISyncMgrSyncItem
 - syncmgr/ISyncMgrSyncItem
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Syncmgr.h
api_name:
 - ISyncMgrSyncItem
---

# ISyncMgrSyncItem interface


## -description

Exposes methods that act on and retrieve information from a single sync item, allowing handlers to manage sync items as independent objects.

## -inheritance

The <b>ISyncMgrSyncItem</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ISyncMgrSyncItem</b> also has these types of members:

## -remarks

A sync item typically represents a group of data, for example, a folder that contains several files. By representing this sync item as an interface, the item can be easily managed and implemented as an object. That object maintains the state of the item when the item is accessed.

Representing a sync item as <b>ISyncMgrSyncItem</b> also allows support for a sync item that contains other sync items.
