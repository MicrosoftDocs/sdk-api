---
UID: NN:syncmgr.ISyncMgrEventLinkUIOperation
title: ISyncMgrEventLinkUIOperation (syncmgr.h)
description: Provides a method that is called when event links are clicked in the sync results folder.
helpviewer_keywords: ["ISyncMgrEventLinkUIOperation","ISyncMgrEventLinkUIOperation interface [Windows Shell]","ISyncMgrEventLinkUIOperation interface [Windows Shell]","described","_shell_ISyncMgrEventLinkUIOperation","shell.ISyncMgrEventLinkUIOperation","syncmgr/ISyncMgrEventLinkUIOperation"]
old-location: shell\ISyncMgrEventLinkUIOperation.htm
tech.root: shell
ms.assetid: 53ea9488-77e0-4eb2-86d3-88747ba44654
ms.date: 12/05/2018
ms.keywords: ISyncMgrEventLinkUIOperation, ISyncMgrEventLinkUIOperation interface [Windows Shell], ISyncMgrEventLinkUIOperation interface [Windows Shell],described, _shell_ISyncMgrEventLinkUIOperation, shell.ISyncMgrEventLinkUIOperation, syncmgr/ISyncMgrEventLinkUIOperation
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
 - ISyncMgrEventLinkUIOperation
 - syncmgr/ISyncMgrEventLinkUIOperation
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
 - ISyncMgrEventLinkUIOperation
---

# ISyncMgrEventLinkUIOperation interface


## -description

Provides a method that is called when event links are clicked in the sync results folder.

## -inheritance

The <b>ISyncMgrEventLinkUIOperation</b> interface inherits from <a href="/windows/desktop/api/syncmgr/nn-syncmgr-isyncmgruioperation">ISyncMgrUIOperation</a>. <b>ISyncMgrEventLinkUIOperation</b> also has these types of members:

## -remarks

This interface also provides the methods of the <a href="/windows/desktop/api/syncmgr/nn-syncmgr-isyncmgruioperation">ISyncMgrUIOperation</a> interface, from which it inherits.

Sync Center calls <a href="/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrhandler-getobject">ISyncMgrHandler::GetObject</a>, specifying SYNCMGR_OBJECTID_EventLinkClick for the object ID.
