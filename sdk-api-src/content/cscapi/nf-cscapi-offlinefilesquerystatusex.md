---
UID: NF:cscapi.OfflineFilesQueryStatusEx
title: OfflineFilesQueryStatusEx function (cscapi.h)
description: Determines whether the Offline Files feature is enabled and, if so, whether it is active and available. This function is identical to the OfflineFilesQueryStatus function, except that it has an additional output parameter.
helpviewer_keywords: ["OfflineFilesQueryStatusEx","OfflineFilesQueryStatusEx function [Offline Files]","cscapi/OfflineFilesQueryStatusEx","of.offlinefilesquerystatusex"]
old-location: of\offlinefilesquerystatusex.htm
tech.root: of
ms.assetid: 1916F3F7-3B99-40CA-B503-EA1D10991BF4
ms.date: 12/05/2018
ms.keywords: OfflineFilesQueryStatusEx, OfflineFilesQueryStatusEx function [Offline Files], cscapi/OfflineFilesQueryStatusEx, of.offlinefilesquerystatusex
req.header: cscapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8
req.target-min-winversvr: Windows Server 2012
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
 - OfflineFilesQueryStatusEx
 - cscapi/OfflineFilesQueryStatusEx
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-fs-cscapi-l1-1-1.dll
 - ext-ms-win-fs-cscapi-l1-1-0.dll
 - CscApi.dll
api_name:
 - OfflineFilesQueryStatusEx
---

# OfflineFilesQueryStatusEx function


## -description

Determines whether the Offline Files feature is enabled and, if so, whether it is active and available. This function is identical to the <a href="/previous-versions/windows/desktop/api/cscapi/nf-cscapi-offlinefilesquerystatus">OfflineFilesQueryStatus</a> function, except that it has an additional output parameter.

## -parameters

### -param pbActive [out]

Receives <b>TRUE</b> if both the CSC driver and Offline Files Service are in the running state, or  <b>FALSE</b> otherwise. This parameter is optional and can be <b>NULL</b>.

### -param pbEnabled [out]

Receives <b>TRUE</b> if the CSC driver's start type is set to <b>SERVICE_SYSTEM_START</b> and the Offline Files service's start type is set to <b>SERVICE_AUTO_START</b>, or <b>FALSE</b> otherwise. This parameter is optional and can be <b>NULL</b>.

### -param pbAvailable [out]

Receives <b>TRUE</b> if the Offline Files Service is ready to be started without requiring the computer to be restarted, or  <b>FALSE</b> otherwise. This parameter is optional and can be <b>NULL</b>.

## -returns

Returns <b>ERROR_SUCCESS</b> if successful or a Win32 error value otherwise.

## -remarks

If the <i>pbAvailable</i> parameter is <b>TRUE</b> on return, the caller can use the <a href="/previous-versions/windows/desktop/api/cscapi/nf-cscapi-offlinefilesstart">OfflineFilesStart</a> function to start the Offline Files feature.

## -see-also

<a href="/previous-versions/windows/desktop/api/cscapi/nf-cscapi-offlinefilesquerystatus">OfflineFilesQueryStatus</a>