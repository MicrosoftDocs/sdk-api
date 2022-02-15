---
UID: NE:mobsync._tagSYNCMGRREGISTERFLAGS
title: SYNCMGRREGISTERFLAGS (mobsync.h)
description: The SYNCMGRREGISTERFLAGS enumeration values are used in methods of the ISyncMgrRegister interface to identify events for which the handler is registered to be notified.
helpviewer_keywords: ["SYNCMGRREGISTERFLAGS","SYNCMGRREGISTERFLAGS enumeration [Windows Shell]","SYNCMGRREGISTERFLAG_CONNECT","SYNCMGRREGISTERFLAG_IDLE","SYNCMGRREGISTERFLAG_PENDINGDISCONNECT","mobsync/SYNCMGRREGISTERFLAGS","mobsync/SYNCMGRREGISTERFLAG_CONNECT","mobsync/SYNCMGRREGISTERFLAG_IDLE","mobsync/SYNCMGRREGISTERFLAG_PENDINGDISCONNECT","shell.syncmgr_SYNCMGRREGISTERFLAGS","syncmgr_SYNCMGRREGISTERFLAGS"]
old-location: shell\syncmgr_SYNCMGRREGISTERFLAGS.htm
tech.root: shell
ms.assetid: be87cebf-da50-437b-bbb1-22c2c764e700
ms.date: 12/05/2018
ms.keywords: SYNCMGRREGISTERFLAGS, SYNCMGRREGISTERFLAGS enumeration [Windows Shell], SYNCMGRREGISTERFLAG_CONNECT, SYNCMGRREGISTERFLAG_IDLE, SYNCMGRREGISTERFLAG_PENDINGDISCONNECT, mobsync/SYNCMGRREGISTERFLAGS, mobsync/SYNCMGRREGISTERFLAG_CONNECT, mobsync/SYNCMGRREGISTERFLAG_IDLE, mobsync/SYNCMGRREGISTERFLAG_PENDINGDISCONNECT, shell.syncmgr_SYNCMGRREGISTERFLAGS, syncmgr_SYNCMGRREGISTERFLAGS
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
req.typenames: SYNCMGRREGISTERFLAGS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _tagSYNCMGRREGISTERFLAGS
 - mobsync/_tagSYNCMGRREGISTERFLAGS
 - SYNCMGRREGISTERFLAGS
 - mobsync/SYNCMGRREGISTERFLAGS
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
 - SYNCMGRREGISTERFLAGS
---

# SYNCMGRREGISTERFLAGS enumeration


## -description

The <b>SYNCMGRREGISTERFLAGS</b> enumeration values are used in methods of the <a href="/windows/desktop/api/mobsync/nn-mobsync-isyncmgrregister">ISyncMgrRegister</a> interface to identify events for which the handler is registered to be notified.

## -enum-fields

### -field SYNCMGRREGISTERFLAG_CONNECT:0x1

Network connect events.

### -field SYNCMGRREGISTERFLAG_PENDINGDISCONNECT:0x2

Pending network disconnect event.

### -field SYNCMGRREGISTERFLAG_IDLE:0x4

Idle events.

## -remarks

The SYNCMGRREGISTERFLAGS_MASK value can be used to identify valid <b>SYNCMGRREGISTERFLAGS</b> values.
