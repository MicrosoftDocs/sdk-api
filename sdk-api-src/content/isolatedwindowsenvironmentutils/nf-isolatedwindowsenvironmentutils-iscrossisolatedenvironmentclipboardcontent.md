---
UID: NF:isolatedwindowsenvironmentutils.IsCrossIsolatedEnvironmentClipboardContent
tech.root: security
title: IsCrossIsolatedEnvironmentClipboardContent
ms.date: 03/06/2023
targetos: Windows
description: Called after an app detects a paste failure to determine if the content being pasted came from the other side of a Windows Defender Application Guard (WDAG) boundary.
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
 - IsCrossIsolatedEnvironmentClipboardContent
f1_keywords:
 - IsCrossIsolatedEnvironmentClipboardContent
 - isolatedwindowsenvironmentutils/IsCrossIsolatedEnvironmentClipboardContent
dev_langs:
 - c++
helpviewer_keywords:
 - IsCrossIsolatedEnvironmentClipboardContent
---

## -description

**IsCrossIsolatedEnvironmentClipboardContent** can be called after an app detects a paste failure to determine if the content being pasted came from the other side of a [Windows Defender Application Guard (WDAG)](/windows/security/threat-protection/microsoft-defender-application-guard/md-app-guard-overview) boundary.

## -parameters

### -param isCrossIsolatedEnvironmentClipboardContent

`[out]`

A pointer to a boolean value that receives the result of the API. This parameter will be `true` if the clipboard content came from the other side of a WDAG boundary, `false` otherwise.

## -returns

If the function succeeds, the return value is `S_OK`. If it fails, it returns an `HRESULT` error code.

## -remarks

This API can be called from both the host and isolated windows environment app instance and can detect both relevant scenarios:

- Scenario 1 -  Called from a host document (ex: pasting content to the host)
  - Returns true if the clipboard content came from any isolated windows environment.
- Scenario 2 -  Called from an isolated windows environment document (ex: pasting content to isolated environment)
  - Returns true if the clipboard content came from the host, or from a different isolated windows environment.

This API also allows apps to continue to show their default paste error handler where appropriate. For example, copy/pasting content within the same isolated environment is not subject to WDAG clipboard policy. Any failure would be due to an unrelated paste error, such as corrupted data. In this case, **IsCrossIsolatedEnvironmentClipboardContent** would return false, so the app knows to follow their default paste error handler flow.

## -see-also

[Microsoft Defender Application Guard overview](/windows/security/threat-protection/microsoft-defender-application-guard/md-app-guard-overview)

[IsolatedWindowsEnvironment](/uwp/api/windows.security.isolation.isolatedwindowsenvironment)

[IsolatedWindowsEnvironmentHost](/uwp/api/windows.security.isolation.isolatedwindowsenvironmenthost)
