---
UID: NE:wtsapi32._WTS_TYPE_CLASS
title: WTS_TYPE_CLASS (wtsapi32.h)
description: Specifies the type of structure that a Remote Desktop Services function has returned in a buffer.
helpviewer_keywords: ["WTSTypeProcessInfoLevel0","WTSTypeProcessInfoLevel1","WTSTypeSessionInfoLevel1","WTS_TYPE_CLASS","WTS_TYPE_CLASS enumeration [Remote Desktop Services]","termserv.wts_type_class","wtsapi32/WTSTypeProcessInfoLevel0","wtsapi32/WTSTypeProcessInfoLevel1","wtsapi32/WTSTypeSessionInfoLevel1","wtsapi32/WTS_TYPE_CLASS"]
old-location: termserv\wts_type_class.htm
tech.root: TermServ
ms.date: 02/10/2026
ms.keywords: WTSTypeProcessInfoLevel0, WTSTypeProcessInfoLevel1, WTSTypeSessionInfoLevel1, WTS_TYPE_CLASS, WTS_TYPE_CLASS enumeration [Remote Desktop Services], termserv.wts_type_class, wtsapi32/WTSTypeProcessInfoLevel0, wtsapi32/WTSTypeProcessInfoLevel1, wtsapi32/WTSTypeSessionInfoLevel1, wtsapi32/WTS_TYPE_CLASS
req.header: wtsapi32.h
req.include-header: 
req.target-type: Windows, version 26100
req.target-min-winverclnt: Windows, version 26100
req.target-min-winversvr: 
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
req.typenames: WTS_TYPE_CLASS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WTS_TYPE_CLASS
 - wtsapi32/_WTS_TYPE_CLASS
 - WTS_TYPE_CLASS
 - wtsapi32/WTS_TYPE_CLASS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wtsapi32.dll
api_name:
 - WTS_TYPE_CLASS
---

## -description

Specifies the type of structure that a Remote Desktop Services function has returned in a buffer.


## -enum-fields

### -field WTSTypeProcessInfoLevel0

The buffer contains the server nonce output by *WTSCloudAuthGetServerNonce*.

### -field WTSTypeProcessInfoLevel1

The buffer contains one or more [WTS_PROCESS_INFO](/windows/desktop/api/wtsapi32/ns-wtsapi32-wts_process_info) structures.

### -field WTSTypeSessionInfoLevel1

The buffer contains the serialized user credential output by [WTSCloudAuthConvertAssertionToSerializedUserCredential](nf-wtsapi32-wtscloudauthduplicateserializedusercredential.md).

### -field WTSTypeCloudAuthServerNonce

The buffer contains one or more [WTS_PROCESS_INFO_EX](/windows/desktop/api/wtsapi32/ns-wtsapi32-wts_process_info_exa) structures

### -field WTSTypeSerializedUserCredential

The buffer contains one or more [WTS_SESSION_INFO_1](/windows/desktop/api/wtsapi32/ns-wtsapi32-wts_session_info_1a) structures.

## -remarks

## -see-also




