---
UID: NS:winbase._EVENTLOG_FULL_INFORMATION
title: EVENTLOG_FULL_INFORMATION (winbase.h)
description: Indicates whether the event log is full.
helpviewer_keywords: ["*LPEVENTLOG_FULL_INFORMATION","EVENTLOG_FULL_INFORMATION","EVENTLOG_FULL_INFORMATION structure","LPEVENTLOG_FULL_INFORMATION","LPEVENTLOG_FULL_INFORMATION structure pointer","_EVENTLOG_FULL_INFORMATION","_win32_eventlog_full_information_str","base.eventlog_full_information_str","winbase/EVENTLOG_FULL_INFORMATION","winbase/LPEVENTLOG_FULL_INFORMATION"]
old-location: base\eventlog_full_information_str.htm
tech.root: base
ms.assetid: 3ca41d6b-51a6-4226-89be-ab2c37628289
ms.date: 12/05/2018
ms.keywords: '*LPEVENTLOG_FULL_INFORMATION, EVENTLOG_FULL_INFORMATION, EVENTLOG_FULL_INFORMATION structure, LPEVENTLOG_FULL_INFORMATION, LPEVENTLOG_FULL_INFORMATION structure pointer, _EVENTLOG_FULL_INFORMATION, _win32_eventlog_full_information_str, base.eventlog_full_information_str, winbase/EVENTLOG_FULL_INFORMATION, winbase/LPEVENTLOG_FULL_INFORMATION'
req.header: winbase.h
req.include-header: Windows.h
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
req.typenames: EVENTLOG_FULL_INFORMATION, *LPEVENTLOG_FULL_INFORMATION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _EVENTLOG_FULL_INFORMATION
 - winbase/_EVENTLOG_FULL_INFORMATION
 - LPEVENTLOG_FULL_INFORMATION
 - winbase/LPEVENTLOG_FULL_INFORMATION
 - EVENTLOG_FULL_INFORMATION
 - winbase/EVENTLOG_FULL_INFORMATION
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winbase.h
api_name:
 - EVENTLOG_FULL_INFORMATION
---

# EVENTLOG_FULL_INFORMATION structure


## -description

Indicates whether the event log is full.

## -struct-fields

### -field dwFull

Indicates whether the event log is full. If the log is full, this member is <b>TRUE</b>. Otherwise, it is <b>FALSE</b>.

## -see-also

<a href="/windows/desktop/api/winbase/nf-winbase-geteventloginformation">GetEventLogInformation</a>