---
UID: NE:mobsync._tagSYNCMGRHANDLERFLAGS
title: SYNCMGRHANDLERFLAGS (mobsync.h)

description: Used in the SYNCMGRHANDLERINFO structure as flags that apply to the current handler.
old-location: shell\syncmgr_syncmgrhandlerflags.htm
tech.root: shell
ms.assetid: 9e5f7f49-f2f0-4fa3-8822-8e6074cd4f47

ms.date: 12/05/2018
ms.keywords: SYNCMGRHANDLERFLAGS, SYNCMGRHANDLERFLAGS enumeration [Windows Shell], SYNCMGRHANDLER_ALWAYSLISTHANDLER, SYNCMGRHANDLER_HASPROPERTIES, SYNCMGRHANDLER_HIDDEN, SYNCMGRHANDLER_MAYESTABLISHCONNECTION, mobsync/SYNCMGRHANDLERFLAGS, mobsync/SYNCMGRHANDLER_ALWAYSLISTHANDLER, mobsync/SYNCMGRHANDLER_HASPROPERTIES, mobsync/SYNCMGRHANDLER_HIDDEN, mobsync/SYNCMGRHANDLER_MAYESTABLISHCONNECTION, shell.syncmgr_syncmgrhandlerflags, syncmgr.syncmgrhandlerflags
ms.topic: enum
f1_keywords:
- mobsync/SYNCMGRHANDLERFLAGS
dev_langs:
 - c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- Mobsync.h
api_name:
- SYNCMGRHANDLERFLAGS
targetos: Windows
req.typenames: SYNCMGRHANDLERFLAGS
req.redist: 
ms.custom: 19H1
---

# SYNCMGRHANDLERFLAGS enumeration


## -description


Used in the <a href="https://docs.microsoft.com/windows/desktop/api/mobsync/ns-mobsync-syncmgrhandlerinfo">SYNCMGRHANDLERINFO</a> structure as flags that apply to the current handler.


## -enum-fields




### -field SYNCMGRHANDLER_HASPROPERTIES

The current handler provides a property sheet dialog.


### -field SYNCMGRHANDLER_MAYESTABLISHCONNECTION

May call back the <a href="https://docs.microsoft.com/windows/desktop/api/mobsync/nf-mobsync-isyncmgrsynchronizecallback-establishconnection">ISyncMgrSynchronizeCallback::EstablishConnection</a> method. This value is ignored in <b>Windows Vista and later</b>.
      


### -field SYNCMGRHANDLER_ALWAYSLISTHANDLER

Indicates Show Handler in Choice even if items are not shown. This value is ignored in <b>Windows Vista and later</b>.
      


### -field SYNCMGRHANDLER_HIDDEN

<b>Windows Vista and later</b>. Do not display handler or item.  This value is ignored by <b>Windows Vista</b>.
      


## -remarks



Only the <b><b>SYNCMGRHANDLER_HASPROPERTIES</b></b> and <b><b>SYNCMGRHANDLER_HIDDEN</b></b> flags are recognized by Windows Vista. Although Windows Vista recognizes the <b><b>SYNCMGRHANDLER_HIDDEN</b></b> flag, it does not currently use it.  

All flags are still valid for previous versions of Windows.
        




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mobsync/ns-mobsync-syncmgrhandlerinfo">SYNCMGRHANDLERINFO</a>
 

 

