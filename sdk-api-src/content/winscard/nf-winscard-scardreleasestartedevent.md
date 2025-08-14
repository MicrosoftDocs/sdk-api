---
UID: NF:winscard.SCardReleaseStartedEvent
title: SCardReleaseStartedEvent function (winscard.h)
description: Decrements the reference count for a handle acquired by a previous call to the SCardAccessStartedEvent function.
helpviewer_keywords: ["SCardReleaseStartedEvent","SCardReleaseStartedEvent function [Security]","_smart_scardreleasestartedevent","security.scardreleasestartedevent","winscard/SCardReleaseStartedEvent"]
old-location: security\scardreleasestartedevent.htm
tech.root: security
ms.assetid: 2c08500f-3ebf-4267-8436-b67543e1c13c
ms.date: 12/05/2018
ms.keywords: SCardReleaseStartedEvent, SCardReleaseStartedEvent function [Security], _smart_scardreleasestartedevent, security.scardreleasestartedevent, winscard/SCardReleaseStartedEvent
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
 - SCardReleaseStartedEvent
 - winscard/SCardReleaseStartedEvent
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
 - SCardReleaseStartedEvent
---

# SCardReleaseStartedEvent function


## -description

The <b>SCardReleaseStartedEvent</b> function decrements the reference count for  a handle acquired by a previous call to the 
<a href="/windows/desktop/api/winscard/nf-winscard-scardaccessstartedevent">SCardAccessStartedEvent</a> function.


