---
UID: NE:mobsync._tagSYNCMGRINVOKEFLAGS
title: SYNCMGRINVOKEFLAGS (mobsync.h)
description: The SYNCMGRINVOKEFLAGS enumeration value specifies how the Sync Manager is to be invoked in the ISyncMgrSynchronizeInvoke::UpdateItems method.
helpviewer_keywords: ["SYNCMGRINVOKEFLAGS","SYNCMGRINVOKEFLAGS enumeration [Windows Shell]","SYNCMGRINVOKE_MINIMIZED","SYNCMGRINVOKE_STARTSYNC","mobsync/SYNCMGRINVOKEFLAGS","mobsync/SYNCMGRINVOKE_MINIMIZED","mobsync/SYNCMGRINVOKE_STARTSYNC","shell.syncmgr_syncmgrinvokeflags","syncmgr.syncmgrinvokeflags"]
old-location: shell\syncmgr_syncmgrinvokeflags.htm
tech.root: shell
ms.assetid: 6526e048-b7a8-4822-afd7-30f04a3039eb
ms.date: 12/05/2018
ms.keywords: SYNCMGRINVOKEFLAGS, SYNCMGRINVOKEFLAGS enumeration [Windows Shell], SYNCMGRINVOKE_MINIMIZED, SYNCMGRINVOKE_STARTSYNC, mobsync/SYNCMGRINVOKEFLAGS, mobsync/SYNCMGRINVOKE_MINIMIZED, mobsync/SYNCMGRINVOKE_STARTSYNC, shell.syncmgr_syncmgrinvokeflags, syncmgr.syncmgrinvokeflags
req.header: mobsync.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.typenames: SYNCMGRINVOKEFLAGS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _tagSYNCMGRINVOKEFLAGS
 - mobsync/_tagSYNCMGRINVOKEFLAGS
 - SYNCMGRINVOKEFLAGS
 - mobsync/SYNCMGRINVOKEFLAGS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mobsync.h
api_name:
 - SYNCMGRINVOKEFLAGS
---

# SYNCMGRINVOKEFLAGS enumeration


## -description

The 
<b>SYNCMGRINVOKEFLAGS</b> enumeration value specifies how the Sync Manager is to be invoked in the 
<a href="/windows/desktop/api/mobsync/nf-mobsync-isyncmgrsynchronizeinvoke-updateitems">ISyncMgrSynchronizeInvoke::UpdateItems</a> method.

## -enum-fields

### -field SYNCMGRINVOKE_STARTSYNC:0x2

Immediately start the synchronization without displaying the <b>Choice</b> dialog box.

### -field SYNCMGRINVOKE_MINIMIZED:0x4

Indicates that the <b>Choice</b> dialog should be minimized by default.

## -see-also

<a href="/windows/desktop/api/mobsync/nf-mobsync-isyncmgrsynchronizeinvoke-updateitems">ISyncMgrSynchronizeInvoke::UpdateItems</a>
