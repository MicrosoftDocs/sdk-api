---
UID: NE:syncmgr.SYNCMGR_RESOLUTION_FEEDBACK
title: SYNCMGR_RESOLUTION_FEEDBACK (syncmgr.h)
description: Describes Sync Manager resolution feedback. Used by ISyncMgrResolutionHandler.
helpviewer_keywords: ["SYNCMGR_RESOLUTION_FEEDBACK","SYNCMGR_RESOLUTION_FEEDBACK enumeration [Windows Shell]","SYNCMGR_RF_CANCEL","SYNCMGR_RF_CONTINUE","SYNCMGR_RF_REFRESH","_shell_SYNCMGR_RESOLUTION_FEEDBACK","shell.SYNCMGR_RESOLUTION_FEEDBACK","syncmgr/SYNCMGR_RESOLUTION_FEEDBACK","syncmgr/SYNCMGR_RF_CANCEL","syncmgr/SYNCMGR_RF_CONTINUE","syncmgr/SYNCMGR_RF_REFRESH"]
old-location: shell\SYNCMGR_RESOLUTION_FEEDBACK.htm
tech.root: shell
ms.assetid: 9526cac8-0df3-40b2-9f86-1a4dadb61dcc
ms.date: 12/05/2018
ms.keywords: SYNCMGR_RESOLUTION_FEEDBACK, SYNCMGR_RESOLUTION_FEEDBACK enumeration [Windows Shell], SYNCMGR_RF_CANCEL, SYNCMGR_RF_CONTINUE, SYNCMGR_RF_REFRESH, _shell_SYNCMGR_RESOLUTION_FEEDBACK, shell.SYNCMGR_RESOLUTION_FEEDBACK, syncmgr/SYNCMGR_RESOLUTION_FEEDBACK, syncmgr/SYNCMGR_RF_CANCEL, syncmgr/SYNCMGR_RF_CONTINUE, syncmgr/SYNCMGR_RF_REFRESH
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
req.typenames: SYNCMGR_RESOLUTION_FEEDBACK
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SYNCMGR_RESOLUTION_FEEDBACK
 - syncmgr/SYNCMGR_RESOLUTION_FEEDBACK
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
 - SYNCMGR_RESOLUTION_FEEDBACK
---

# SYNCMGR_RESOLUTION_FEEDBACK enumeration


## -description

Describes Sync Manager resolution feedback. Used by <a href="/windows/desktop/api/syncmgr/nn-syncmgr-isyncmgrresolutionhandler">ISyncMgrResolutionHandler</a>.

## -enum-fields

### -field SYNCMGR_RF_CONTINUE:0

Proceed to the next conflict.

### -field SYNCMGR_RF_REFRESH

<b>Apply to All</b> is stopped and the dialog will be displayed for this conflict.

### -field SYNCMGR_RF_CANCEL

 Cancels resolution of any more conflicts in the set.
