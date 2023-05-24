---
UID: NF:winsafer.SaferRecordEventLogEntry
title: SaferRecordEventLogEntry function (winsafer.h)
description: Saves messages to an event log.
helpviewer_keywords: ["SaferRecordEventLogEntry","SaferRecordEventLogEntry function [Security]","_mnp_saferrecordeventlogentry","security.saferrecordeventlogentry","winsafer/SaferRecordEventLogEntry"]
old-location: security\saferrecordeventlogentry.htm
tech.root: security
ms.assetid: 7eb48f80-3a57-46ec-aca1-6ff8c1c514c6
ms.date: 12/05/2018
ms.keywords: SaferRecordEventLogEntry, SaferRecordEventLogEntry function [Security], _mnp_saferrecordeventlogentry, security.saferrecordeventlogentry, winsafer/SaferRecordEventLogEntry
req.header: winsafer.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SaferRecordEventLogEntry
 - winsafer/SaferRecordEventLogEntry
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Advapi32.dll
api_name:
 - SaferRecordEventLogEntry
req.apiset: ext-ms-win-advapi32-safer-l1-1-0 (introduced in Windows 8)
---

# SaferRecordEventLogEntry function


## -description

The <b>SaferRecordEventLogEntry</b> function saves messages to an event log.

## -parameters

### -param hLevel [in]

SAFER_LEVEL_HANDLE that contains the details of the rule to send to the event log.

### -param szTargetPath [in]

Path of the file that attempted to run.

### -param lpReserved

Reserved for future use. This parameter should be set to <b>NULL</b>.

## -returns

<b>TRUE</b> if the function succeeds; otherwise, <b>FALSE</b>. For extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

If <a href="/windows/desktop/api/winsafer/nf-winsafer-saferidentifylevel">SaferIdentifyLevel</a> returns a SAFER_LEVEL_HANDLE with a LevelId that is anything other than SAFER_LEVELID_FULLYTRUSTED (0x40000), <b>SaferRecordEventLogEntry</b> can be called to facilitate troubleshooting. For example, clicking a button in excel.exe might attempt to launch another process that is not fully trusted. This might display an obscure error message because the program remapped the error returned from CreateProcess. To ease troubleshooting, some Safer functions call <b>SaferRecordEventLogEntry</b> to send an event to the event log.
