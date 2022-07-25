---
UID: NE:syncmgr.SYNCMGR_CANCEL_REQUEST
title: SYNCMGR_CANCEL_REQUEST (syncmgr.h)
description: Describes a request by the user to cancel a synchronization.
helpviewer_keywords: ["SYNCMGR_CANCEL_REQUEST","SYNCMGR_CANCEL_REQUEST enumeration [Windows Shell]","SYNCMGR_CR_CANCEL_ALL","SYNCMGR_CR_CANCEL_ITEM","SYNCMGR_CR_MAX","SYNCMGR_CR_NONE","shell.SYNCMGR_CANCEL_REQUEST","shell_SYNCMGR_CANCEL_REQUEST","syncmgr/SYNCMGR_CANCEL_REQUEST","syncmgr/SYNCMGR_CR_CANCEL_ALL","syncmgr/SYNCMGR_CR_CANCEL_ITEM","syncmgr/SYNCMGR_CR_MAX","syncmgr/SYNCMGR_CR_NONE"]
old-location: shell\SYNCMGR_CANCEL_REQUEST.htm
tech.root: shell
ms.assetid: 81cf8dcc-c847-41e0-82e2-b5f547fc03cf
ms.date: 12/05/2018
ms.keywords: SYNCMGR_CANCEL_REQUEST, SYNCMGR_CANCEL_REQUEST enumeration [Windows Shell], SYNCMGR_CR_CANCEL_ALL, SYNCMGR_CR_CANCEL_ITEM, SYNCMGR_CR_MAX, SYNCMGR_CR_NONE, shell.SYNCMGR_CANCEL_REQUEST, shell_SYNCMGR_CANCEL_REQUEST, syncmgr/SYNCMGR_CANCEL_REQUEST, syncmgr/SYNCMGR_CR_CANCEL_ALL, syncmgr/SYNCMGR_CR_CANCEL_ITEM, syncmgr/SYNCMGR_CR_MAX, syncmgr/SYNCMGR_CR_NONE
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
req.typenames: SYNCMGR_CANCEL_REQUEST
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SYNCMGR_CANCEL_REQUEST
 - syncmgr/SYNCMGR_CANCEL_REQUEST
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Syncmgr.h
api_name:
 - SYNCMGR_CANCEL_REQUEST
---

# SYNCMGR_CANCEL_REQUEST enumeration


## -description

Describes a request by the user to cancel a synchronization.

## -enum-fields

### -field SYNCMGR_CR_NONE:0

No cancelation request has been made.

### -field SYNCMGR_CR_CANCEL_ITEM:1

Stop the synchronization of the current item, but continue the synchronization of other items.

### -field SYNCMGR_CR_CANCEL_ALL:2

Stop the synchronization entirely.

### -field SYNCMGR_CR_MAX

The maximum valid <a href="/windows/desktop/api/syncmgr/ne-syncmgr-syncmgr_cancel_request">SYNCMGR_CANCEL_REQUEST</a> value.
