---
UID: NE:mobsync._tagSYNCMGRREGISTERFLAGS
title: "_tagSYNCMGRREGISTERFLAGS"
author: windows-sdk-content
description: The SYNCMGRREGISTERFLAGS enumeration values are used in methods of the ISyncMgrRegister interface to identify events for which the handler is registered to be notified.
old-location: shell\syncmgr_SYNCMGRREGISTERFLAGS.htm
tech.root: shell
ms.assetid: be87cebf-da50-437b-bbb1-22c2c764e700
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: SYNCMGRREGISTERFLAGS, SYNCMGRREGISTERFLAGS enumeration [Windows Shell], SYNCMGRREGISTERFLAG_CONNECT, SYNCMGRREGISTERFLAG_IDLE, SYNCMGRREGISTERFLAG_PENDINGDISCONNECT, _tagSYNCMGRREGISTERFLAGS, mobsync/SYNCMGRREGISTERFLAGS, mobsync/SYNCMGRREGISTERFLAG_CONNECT, mobsync/SYNCMGRREGISTERFLAG_IDLE, mobsync/SYNCMGRREGISTERFLAG_PENDINGDISCONNECT, shell.syncmgr_SYNCMGRREGISTERFLAGS, syncmgr_SYNCMGRREGISTERFLAGS
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
 - SYNCMGRREGISTERFLAGS
product: Windows
targetos: Windows
req.typenames: SYNCMGRREGISTERFLAGS
req.redist: 
---

# _tagSYNCMGRREGISTERFLAGS enumeration


## -description


The <b>SYNCMGRREGISTERFLAGS</b> enumeration values are used in methods of the <a href="https://msdn.microsoft.com/1feed230-5a50-4ff5-a8a9-e0ce15ba8f1c">ISyncMgrRegister</a> interface to identify events for which the handler is registered to be notified.


## -enum-fields




### -field SYNCMGRREGISTERFLAG_CONNECT

Network connect events.


### -field SYNCMGRREGISTERFLAG_PENDINGDISCONNECT

Pending network disconnect event.


### -field SYNCMGRREGISTERFLAG_IDLE

Idle events.


## -remarks



The SYNCMGRREGISTERFLAGS_MASK value can be used to identify valid <b>SYNCMGRREGISTERFLAGS</b> values.



