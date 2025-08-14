---
UID: NF:networkisolation.NetworkIsolationDiagnoseConnectFailure
title: NetworkIsolationDiagnoseConnectFailure
description: Determines whether the calling application has the required AppContainer capabilities to make a network connection to a target server.
ms.date: 05/06/2024
tech.root: ics
targetos: Windows
prerelease: false
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: networkisolation.h
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
 - HeaderDef
api_location:
 - api-ms-win-net-isolation-l1-1-1.dll
 - networkisolation.h
api_name:
 - NetworkIsolationDiagnoseConnectFailure
f1_keywords:
 - NetworkIsolationDiagnoseConnectFailure
 - networkisolation/NetworkIsolationDiagnoseConnectFailure
dev_langs:
 - c++
helpviewer_keywords:
 - NetworkIsolationDiagnoseConnectFailure
---

## -description

Determines whether the calling application has the required [AppContainer](/windows/win32/secauthz/appcontainer-for-legacy-applications-) capabilities to make a network connection to a target server. Depending on the resolution of the server name, the function checks for **internetClient**, **internetClientServer**, and **privateNetworkClientServer**. For more info, see [App capability declarations](/windows/uwp/packaging/app-capability-declarations).

## -parameters

### -param wszServerName

Type: \_\_in **[LPCWSTR](/windows/win32/winprog/windows-data-types)**

The name of the target server.

## -returns

Type: **[DWORD](/windows/win32/winprog/windows-data-types)**

**TRUE** if the calling application has the required capabilities for the target server; otherwise, **FALSE**.

## -remarks

## -see-also
