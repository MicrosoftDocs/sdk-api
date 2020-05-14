---
UID: NE:syncmgr.SYNCMGR_HANDLER_TYPE
title: SYNCMGR_HANDLER_TYPE (syncmgr.h)
description: Specifies the type of a handler. Used by ISyncMgrHandlerInfo::GetType.helpviewer_keywords: ["SYNCMGR_HANDLER_TYPE","SYNCMGR_HANDLER_TYPE enumeration [Windows Shell]","SYNCMGR_HT_APPLICATION","SYNCMGR_HT_COMPUTER","SYNCMGR_HT_DEVICE","SYNCMGR_HT_FOLDER","SYNCMGR_HT_MAX","SYNCMGR_HT_MIN","SYNCMGR_HT_SERVICE","SYNCMGR_HT_UNSPECIFIED","shell.SYNCMGR_HANDLER_TYPE","shell_SYNCMGR_HANDLER_TYPE","syncmgr/SYNCMGR_HANDLER_TYPE","syncmgr/SYNCMGR_HT_APPLICATION","syncmgr/SYNCMGR_HT_COMPUTER","syncmgr/SYNCMGR_HT_DEVICE","syncmgr/SYNCMGR_HT_FOLDER","syncmgr/SYNCMGR_HT_MAX","syncmgr/SYNCMGR_HT_MIN","syncmgr/SYNCMGR_HT_SERVICE","syncmgr/SYNCMGR_HT_UNSPECIFIED"]
old-location: shell\SYNCMGR_HANDLER_TYPE.htm
tech.root: shell
ms.assetid: 993a1d55-32ee-4ea7-823f-a533e9646f1f
ms.date: 12/05/2018
ms.keywords: SYNCMGR_HANDLER_TYPE, SYNCMGR_HANDLER_TYPE enumeration [Windows Shell], SYNCMGR_HT_APPLICATION, SYNCMGR_HT_COMPUTER, SYNCMGR_HT_DEVICE, SYNCMGR_HT_FOLDER, SYNCMGR_HT_MAX, SYNCMGR_HT_MIN, SYNCMGR_HT_SERVICE, SYNCMGR_HT_UNSPECIFIED, shell.SYNCMGR_HANDLER_TYPE, shell_SYNCMGR_HANDLER_TYPE, syncmgr/SYNCMGR_HANDLER_TYPE, syncmgr/SYNCMGR_HT_APPLICATION, syncmgr/SYNCMGR_HT_COMPUTER, syncmgr/SYNCMGR_HT_DEVICE, syncmgr/SYNCMGR_HT_FOLDER, syncmgr/SYNCMGR_HT_MAX, syncmgr/SYNCMGR_HT_MIN, syncmgr/SYNCMGR_HT_SERVICE, syncmgr/SYNCMGR_HT_UNSPECIFIED
f1_keywords:
- syncmgr/SYNCMGR_HANDLER_TYPE
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- Syncmgr.h
api_name:
- SYNCMGR_HANDLER_TYPE
targetos: Windows
req.typenames: SYNCMGR_HANDLER_TYPE
req.redist: 
ms.custom: 19H1
---

# SYNCMGR_HANDLER_TYPE enumeration


## -description


Specifies the type of a handler. Used by <a href="https://docs.microsoft.com/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrhandlerinfo-gettype">ISyncMgrHandlerInfo::GetType</a>.


## -enum-fields




### -field SYNCMGR_HT_UNSPECIFIED

The handler type is unknown. This value is also used if <a href="https://docs.microsoft.com/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrhandlerinfo-gettype">ISyncMgrHandlerInfo::GetType</a> fails.


### -field SYNCMGR_HT_APPLICATION

The handler is an application.


### -field SYNCMGR_HT_DEVICE

The handler syncs with a device such as a phone or PDA.


### -field SYNCMGR_HT_FOLDER

The handler syncs with local or remote folders.


### -field SYNCMGR_HT_SERVICE

The handler syncs with a web service.


### -field SYNCMGR_HT_COMPUTER

The handler syncs with a computer.


### -field SYNCMGR_HT_MIN

Indicates the minimum <a href="https://docs.microsoft.com/windows/desktop/api/syncmgr/ne-syncmgr-syncmgr_handler_type">SYNCMGR_HANDLER_TYPE</a> value.


### -field SYNCMGR_HT_MAX

Indicates the maximum <a href="https://docs.microsoft.com/windows/desktop/api/syncmgr/ne-syncmgr-syncmgr_handler_type">SYNCMGR_HANDLER_TYPE</a> value.

