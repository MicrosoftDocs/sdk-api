---
UID: NF:cscapi.OfflineFilesQueryStatus
title: OfflineFilesQueryStatus function (cscapi.h)
description: Determines whether the Offline Files feature is enabled and, if so, whether it is active.
helpviewer_keywords: ["OfflineFilesQueryStatus","OfflineFilesQueryStatus function [Offline Files]","cscapi/OfflineFilesQueryStatus","of.offlinefilesquerystatus"]
old-location: of\offlinefilesquerystatus.htm
tech.root: of
ms.assetid: 2b3a77cd-e874-42fb-8bfa-6d6b26866153
ms.date: 12/05/2018
ms.keywords: OfflineFilesQueryStatus, OfflineFilesQueryStatus function [Offline Files], cscapi/OfflineFilesQueryStatus, of.offlinefilesquerystatus
req.header: cscapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: CscApi.lib
req.dll: CscApi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - OfflineFilesQueryStatus
 - cscapi/OfflineFilesQueryStatus
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-fs-cscapi-l1-1-1.dll
 - CscApi.dll
api_name:
 - OfflineFilesQueryStatus
---

# OfflineFilesQueryStatus function


## -description

Determines whether the Offline Files feature is enabled and, if so, whether it is active.

## -parameters

### -param pbActive [out]

Receives <b>TRUE</b> if both the CSC driver and Offline Files Service are in the running state, or  <b>FALSE</b> otherwise. This parameter is optional and can be <b>NULL</b>.

### -param pbEnabled [out]

Receives <b>TRUE</b> if the CSC driver's start type is set to <b>SERVICE_SYSTEM_START</b> and the Offline Files service's start type is set to <b>SERVICE_AUTO_START</b>, or <b>FALSE</b> otherwise. This parameter is optional and can be <b>NULL</b>.

## -returns

Returns <b>ERROR_SUCCESS</b> if successful or a Win32 error value otherwise.

## -remarks

If the values returned in the <i>pbActive</i> and <i>pbEnabled</i> parameters are not both <b>TRUE</b>, the caller must restart the computer to enable or disable the Offline Files feature.  If one of the values is still <b>FALSE</b> after the computer is restarted, check the system event logs to identify the problem with starting either the CSC driver or the Offline Files service.

## -see-also

<a href="/previous-versions/windows/desktop/api/cscapi/nf-cscapi-offlinefilesquerystatusex">OfflineFilesQueryStatusEx</a>