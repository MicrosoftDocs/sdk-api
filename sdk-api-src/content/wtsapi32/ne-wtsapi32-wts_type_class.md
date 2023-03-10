---
UID: NE:wtsapi32._WTS_TYPE_CLASS
title: WTS_TYPE_CLASS (wtsapi32.h)
description: Specifies the type of structure that a Remote Desktop Services function has returned in a buffer.
helpviewer_keywords: ["WTSTypeProcessInfoLevel0","WTSTypeProcessInfoLevel1","WTSTypeSessionInfoLevel1","WTS_TYPE_CLASS","WTS_TYPE_CLASS enumeration [Remote Desktop Services]","termserv.wts_type_class","wtsapi32/WTSTypeProcessInfoLevel0","wtsapi32/WTSTypeProcessInfoLevel1","wtsapi32/WTSTypeSessionInfoLevel1","wtsapi32/WTS_TYPE_CLASS"]
old-location: termserv\wts_type_class.htm
tech.root: TermServ
ms.assetid: 1827e862-add0-4271-b5d7-62834c396250
ms.date: 12/05/2018
ms.keywords: WTSTypeProcessInfoLevel0, WTSTypeProcessInfoLevel1, WTSTypeSessionInfoLevel1, WTS_TYPE_CLASS, WTS_TYPE_CLASS enumeration [Remote Desktop Services], termserv.wts_type_class, wtsapi32/WTSTypeProcessInfoLevel0, wtsapi32/WTSTypeProcessInfoLevel1, wtsapi32/WTSTypeSessionInfoLevel1, wtsapi32/WTS_TYPE_CLASS
req.header: wtsapi32.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7
req.target-min-winversvr: Windows Server 2008 R2
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
 - Wtsapi32.h
api_name:
 - WTS_TYPE_CLASS
---

# WTS_TYPE_CLASS enumeration


## -description

Specifies the type of structure that a Remote Desktop Services function has returned in a buffer.

## -enum-fields

### -field WTSTypeProcessInfoLevel0

The buffer contains one or more <a href="/windows/desktop/api/wtsapi32/ns-wtsapi32-wts_process_infoa">WTS_PROCESS_INFO</a> structures.

### -field WTSTypeProcessInfoLevel1

The buffer contains one or more <a href="/windows/desktop/api/wtsapi32/ns-wtsapi32-wts_process_info_exa">WTS_PROCESS_INFO_EX</a> structures.

### -field WTSTypeSessionInfoLevel1

The buffer contains one or more <a href="/windows/desktop/api/wtsapi32/ns-wtsapi32-wts_session_info_1a">WTS_SESSION_INFO_1</a> structures.

## -see-also

<a href="/windows/desktop/api/wtsapi32/nf-wtsapi32-wtsfreememory">WTSFreeMemory</a>



<a href="/windows/desktop/api/wtsapi32/nf-wtsapi32-wtsfreememoryexa">WTSFreeMemoryEx</a>