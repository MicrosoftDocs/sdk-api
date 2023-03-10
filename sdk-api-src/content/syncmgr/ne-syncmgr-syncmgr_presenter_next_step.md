---
UID: NE:syncmgr.SYNCMGR_PRESENTER_NEXT_STEP
title: SYNCMGR_PRESENTER_NEXT_STEP (syncmgr.h)
description: Describes the next step that is to occur in sync manager conflict resolution. Used by ISyncMgrConflictPresenter.
helpviewer_keywords: ["SYNCMGR_PNS_CANCEL","SYNCMGR_PNS_CONTINUE","SYNCMGR_PNS_DEFAULT","SYNCMGR_PRESENTER_NEXT_STEP","SYNCMGR_PRESENTER_NEXT_STEP enumeration [Windows Shell]","_shell_SYNCMGR_PRESENTER_NEXT_STEP","shell.SYNCMGR_PRESENTER_NEXT_STEP","syncmgr/SYNCMGR_PNS_CANCEL","syncmgr/SYNCMGR_PNS_CONTINUE","syncmgr/SYNCMGR_PNS_DEFAULT","syncmgr/SYNCMGR_PRESENTER_NEXT_STEP"]
old-location: shell\SYNCMGR_PRESENTER_NEXT_STEP.htm
tech.root: shell
ms.assetid: e24b09e0-38a1-421b-8cf1-74f553cf93e7
ms.date: 12/05/2018
ms.keywords: SYNCMGR_PNS_CANCEL, SYNCMGR_PNS_CONTINUE, SYNCMGR_PNS_DEFAULT, SYNCMGR_PRESENTER_NEXT_STEP, SYNCMGR_PRESENTER_NEXT_STEP enumeration [Windows Shell], _shell_SYNCMGR_PRESENTER_NEXT_STEP, shell.SYNCMGR_PRESENTER_NEXT_STEP, syncmgr/SYNCMGR_PNS_CANCEL, syncmgr/SYNCMGR_PNS_CONTINUE, syncmgr/SYNCMGR_PNS_DEFAULT, syncmgr/SYNCMGR_PRESENTER_NEXT_STEP
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
req.typenames: SYNCMGR_PRESENTER_NEXT_STEP
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SYNCMGR_PRESENTER_NEXT_STEP
 - syncmgr/SYNCMGR_PRESENTER_NEXT_STEP
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
 - SYNCMGR_PRESENTER_NEXT_STEP
---

# SYNCMGR_PRESENTER_NEXT_STEP enumeration


## -description

Describes the next step that is to occur in sync manager conflict resolution. Used by <a href="/windows/desktop/api/syncmgr/nn-syncmgr-isyncmgrconflictpresenter">ISyncMgrConflictPresenter</a>.

## -enum-fields

### -field SYNCMGR_PNS_CONTINUE:0

The conflict has been resolved and subsequent
selected conflicts should continue to be resolved.

### -field SYNCMGR_PNS_DEFAULT

The default conflict presenter should be used.

### -field SYNCMGR_PNS_CANCEL

All conflict resolution should be canceled.

## -see-also

<a href="/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrconflictresolveinfo-getpresenternextstep">ISyncMgrConflictResolveInfo::GetPresenterNextStep</a>



<a href="/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrconflictresolveinfo-setpresenternextstep">ISyncMgrConflictResolveInfo::SetPresenterNextStep</a>
