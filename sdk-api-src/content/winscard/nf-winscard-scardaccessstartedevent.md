---
UID: NF:winscard.SCardAccessStartedEvent
title: SCardAccessStartedEvent function (winscard.h)
description: Returns an event handle when an event signals that the smart card resource manager is started.
helpviewer_keywords: ["SCardAccessStartedEvent","SCardAccessStartedEvent function [Security]","_smart_scardaccessstartedevent","security.scardaccessstartedevent","winscard/SCardAccessStartedEvent"]
old-location: security\scardaccessstartedevent.htm
tech.root: security
ms.assetid: ddfab09d-5477-4c4e-883c-d3c19258c49d
ms.date: 12/05/2018
ms.keywords: SCardAccessStartedEvent, SCardAccessStartedEvent function [Security], _smart_scardaccessstartedevent, security.scardaccessstartedevent, winscard/SCardAccessStartedEvent
req.header: winscard.h
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
req.lib: Winscard.lib
req.dll: Winscard.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SCardAccessStartedEvent
 - winscard/SCardAccessStartedEvent
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-security-winscard-l1-1-1.dll
 - Winscard.dll
 - Ext-MS-Win-Security-WinSCard-L1-1-0.dll
api_name:
 - SCardAccessStartedEvent
---

# SCardAccessStartedEvent function


## -description

The <b>SCardAccessStartedEvent</b> function returns an event handle when an event signals that the smart card resource manager is started. The event-object handle can be specified in a call to one of the wait functions.



## -returns

The function returns an event HANDLE if it succeeds or <b>NULL</b> if it fails.

 If the function fails, the <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function provides information on the cause of the failure.

## -remarks

The event-object handle returned can be specified in a call to one of the wait functions.

Do not close the handle returned by this function.
When you have finished using the handle, decrement the reference count by calling the <a href="/windows/desktop/api/winscard/nf-winscard-scardreleasestartedevent">SCardReleaseStartedEvent</a> function.
