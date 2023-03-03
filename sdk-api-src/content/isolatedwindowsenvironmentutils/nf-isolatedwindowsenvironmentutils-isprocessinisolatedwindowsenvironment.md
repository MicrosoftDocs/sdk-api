---
UID: NF:isolatedwindowsenvironmentutils.IsProcessInIsolatedWindowsEnvironment
tech.root: security
title: IsProcessInIsolatedWindowsEnvironment
ms.date: 03/06/2023
targetos: Windows
description: Determines in which execution environment the application is running.
prerelease: false
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: isolatedwindowsenvironmentutils.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - 
api_location:
 - isolatedwindowsenvironmentutils.h
api_name:
 - IsProcessInIsolatedWindowsEnvironment
f1_keywords:
 - IsProcessInIsolatedWindowsEnvironment
 - isolatedwindowsenvironmentutils/IsProcessInIsolatedWindowsEnvironment
dev_langs:
 - c++
helpviewer_keywords:
 - IsProcessInIsolatedWindowsEnvironment
---

## -description

Determines in which execution environment the application is running – a host or an Isolated Environment.

## -parameters

### -param isProcessInIsolatedWindowsEnvironment

`[out]`

A pointer to a boolean value that receives the result of the API. This parameter will be `true` if the process is in an isolated Windows environment, `false` otherwise.

## -returns

Returns `S_OK` if the function succeeds. If it fails, it returns an `HRESULT` error code.

## -remarks

Any application using [Windows Defender Application Guard (WDAG)](/windows/security/threat-protection/microsoft-defender-application-guard/md-app-guard-overview) will require the ability to find which execution environment it is running in. This is needed so that the app can behave appropriately to protect user/enterprise data, user identity, and the business interests of the app.

## -see-also

[Microsoft Defender Application Guard overview](/windows/security/threat-protection/microsoft-defender-application-guard/md-app-guard-overview)

[IsolatedWindowsEnvironment](/uwp/api/windows.security.isolation.isolatedwindowsenvironment)

[IsolatedWindowsEnvironmentHost](/uwp/api/windows.security.isolation.isolatedwindowsenvironmenthost)
