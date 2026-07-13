---
UID: NF:versionhelpers.IsActiveSessionCountLimited
tech.root: 
title: IsActiveSessionCountLimited
ms.date: 
targetos: Windows
description: 
prerelease: false
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: Kernel32.dll; Ntdll.dll
req.header: versionhelpers.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: Kernel32.lib; Ntdll.lib
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 10
req.target-min-winversvr: Windows Server 2016
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - versionhelpers.h
api_name:
 - IsActiveSessionCountLimited
f1_keywords:
 - IsActiveSessionCountLimited
 - versionhelpers/IsActiveSessionCountLimited
dev_langs:
 - c++
helpviewer_keywords:
 - IsActiveSessionCountLimited
---

## -description

Indicates if the current OS allows only a limited number of concurrent interactive sessions.

## -returns

True if the current OS limits the number of concurrent interactive sessions; otherwise, false.

## -remarks

Most editions of Windows have a limit on the number of concurrent interactive sessions. Some editions of Windows&mdash;like Windows 10 Enterprise multi-session, Windows 11 Enterprise multi-session, and some editions of Windows Server&mdash;support an unlimited number of concurrent interactive session. This function returns true if there is a limit in place.

On Windows Server, this functions returns false only when the Remote Desktop Session Host role is installed.

## -see-also

<a href="/azure/virtual-desktop/windows-multisession-faq">Windows Enterprise multi-session FAQ</a>
