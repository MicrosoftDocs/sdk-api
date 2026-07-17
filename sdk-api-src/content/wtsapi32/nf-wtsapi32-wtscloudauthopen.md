---
UID: NF:wtsapi32.WTSCloudAuthOpen
tech.root: TermServ
title: WTSCloudAuthOpen
ms.date: 09/25/2025
targetos: Windows
description: Obtains a cloud authentication handle.
prerelease: false
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: wtsapi32.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows, version 26100
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
 - wtsapi32.dll
api_name:
 - WTSCloudAuthOpen
f1_keywords:
 - WTSCloudAuthOpen
 - wtsapi32/WTSCloudAuthOpen
dev_langs:
 - c++
helpviewer_keywords:
 - WTSCloudAuthOpen
---

## -description

Obtains a cloud authentication handle. To call this function successfully, the calling application must be running within the context of the `NetworkService` or `LocalSystem` account.

## -parameters

### -param activityId [in]

A pointer to a GUID to uniquely identify events related to this operation in Event Viewer. The caller chooses this GUID for their convenience.

## -returns

If the function succeeds, the return value is a valid cloud authentication handle. It should be closed by calling *[WTSCloudAuthClose](./nf-wtsapi32-wtscloudauthclose.md)*. If the function fails, the return value is `NULL`. To get extended error information, call the [`GetLastError`](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) function.

## -remarks

A cloud authentication handle can be used for remote Entra ID authentication and authorization purposes using the `WTSCloudAuth*` API family.

## -see-also

