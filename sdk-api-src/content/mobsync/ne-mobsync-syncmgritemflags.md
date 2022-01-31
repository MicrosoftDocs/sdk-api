---
UID: NE:mobsync._tagSYNCMGRITEMFLAGS
title: SYNCMGRITEMFLAGS (mobsync.h)
description: Specifies information for the current item in the SYNCMGRITEM structure.
helpviewer_keywords: ["SYNCMGRITEMFLAGS","SYNCMGRITEMFLAGS enumeration [Windows Shell]","SYNCMGRITEM_HASPROPERTIES","SYNCMGRITEM_HIDDEN","SYNCMGRITEM_LASTUPDATETIME","SYNCMGRITEM_MAYDELETEITEM","SYNCMGRITEM_ROAMINGUSER","SYNCMGRITEM_TEMPORARY","mobsync/SYNCMGRITEMFLAGS","mobsync/SYNCMGRITEM_HASPROPERTIES","mobsync/SYNCMGRITEM_HIDDEN","mobsync/SYNCMGRITEM_LASTUPDATETIME","mobsync/SYNCMGRITEM_MAYDELETEITEM","mobsync/SYNCMGRITEM_ROAMINGUSER","mobsync/SYNCMGRITEM_TEMPORARY","shell.syncmgr_syncmgritemflags","syncmgr.syncmgritemflags"]
old-location: shell\syncmgr_syncmgritemflags.htm
tech.root: shell
ms.assetid: 6297f10b-9a2c-4077-9dca-e5c0850d125a
ms.date: 12/05/2018
ms.keywords: SYNCMGRITEMFLAGS, SYNCMGRITEMFLAGS enumeration [Windows Shell], SYNCMGRITEM_HASPROPERTIES, SYNCMGRITEM_HIDDEN, SYNCMGRITEM_LASTUPDATETIME, SYNCMGRITEM_MAYDELETEITEM, SYNCMGRITEM_ROAMINGUSER, SYNCMGRITEM_TEMPORARY, mobsync/SYNCMGRITEMFLAGS, mobsync/SYNCMGRITEM_HASPROPERTIES, mobsync/SYNCMGRITEM_HIDDEN, mobsync/SYNCMGRITEM_LASTUPDATETIME, mobsync/SYNCMGRITEM_MAYDELETEITEM, mobsync/SYNCMGRITEM_ROAMINGUSER, mobsync/SYNCMGRITEM_TEMPORARY, shell.syncmgr_syncmgritemflags, syncmgr.syncmgritemflags
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
req.typenames: SYNCMGRITEMFLAGS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _tagSYNCMGRITEMFLAGS
 - mobsync/_tagSYNCMGRITEMFLAGS
 - SYNCMGRITEMFLAGS
 - mobsync/SYNCMGRITEMFLAGS
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
 - SYNCMGRITEMFLAGS
---

# SYNCMGRITEMFLAGS enumeration


## -description

Specifies information for the current item in the <a href="/windows/desktop/api/mobsync/ns-mobsync-syncmgritem">SYNCMGRITEM</a> structure.

## -enum-fields

### -field SYNCMGRITEM_HASPROPERTIES:0x1

The item has a properties dialog.

### -field SYNCMGRITEM_TEMPORARY:0x2

The item is temporary and any stored preferences can be removed. This value is defined but not used in Windows Vista.

### -field SYNCMGRITEM_ROAMINGUSER:0x4

The item roams with the user and is not specific to a machine. This value is defined but is ignored by both Windows XP and Windows Vista.

### -field SYNCMGRITEM_LASTUPDATETIME:0x8

The LastUpdateTime field is valid.

### -field SYNCMGRITEM_MAYDELETEITEM:0x10

The item may be deleted. This value has been deprecated for Windows Vista and later. This value is defined but is ignored by both Windows XP and Windows Vista.

### -field SYNCMGRITEM_HIDDEN:0x20

<b>Windows Vista and later</b>. Not supported.

## -see-also

<a href="/windows/desktop/api/mobsync/ns-mobsync-syncmgritem">SYNCMGRITEM</a>
