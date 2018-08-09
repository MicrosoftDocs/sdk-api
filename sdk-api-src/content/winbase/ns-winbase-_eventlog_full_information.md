---
UID: NS:winbase._EVENTLOG_FULL_INFORMATION
title: "_EVENTLOG_FULL_INFORMATION"
author: windows-sdk-content
description: Indicates whether the event log is full.
old-location: base\eventlog_full_information_str.htm
old-project: eventlog
ms.assetid: 3ca41d6b-51a6-4226-89be-ab2c37628289
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: "*LPEVENTLOG_FULL_INFORMATION, EVENTLOG_FULL_INFORMATION, EVENTLOG_FULL_INFORMATION structure, LPEVENTLOG_FULL_INFORMATION, LPEVENTLOG_FULL_INFORMATION structure pointer, _EVENTLOG_FULL_INFORMATION, _win32_eventlog_full_information_str, base.eventlog_full_information_str, winbase/EVENTLOG_FULL_INFORMATION, winbase/LPEVENTLOG_FULL_INFORMATION"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
tech.root: 
req.typenames: EVENTLOG_FULL_INFORMATION, *LPEVENTLOG_FULL_INFORMATION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winbase.h
api_name:
 - EVENTLOG_FULL_INFORMATION
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _EVENTLOG_FULL_INFORMATION structure


## -description


Indicates whether the event log is full.


## -struct-fields




### -field dwFull

Indicates whether the event log is full. If the log is full, this member is <b>TRUE</b>. Otherwise, it is <b>FALSE</b>.


## -see-also




<a href="https://msdn.microsoft.com/627e0af2-3ce6-47fe-89c6-d7c0483cb94b">GetEventLogInformation</a>
 

 

