---
UID: NF:cscapi.OfflineFilesEnable
title: OfflineFilesEnable function (cscapi.h)
description: Enables or disables the Offline Files feature.
helpviewer_keywords: ["OfflineFilesEnable","OfflineFilesEnable function [Offline Files]","cscapi/OfflineFilesEnable","of.offlinefilesenable"]
old-location: of\offlinefilesenable.htm
tech.root: of
ms.assetid: ea29b1f5-3f7e-479a-9409-f63c708d9c64
ms.date: 12/05/2018
ms.keywords: OfflineFilesEnable, OfflineFilesEnable function [Offline Files], cscapi/OfflineFilesEnable, of.offlinefilesenable
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
 - OfflineFilesEnable
 - cscapi/OfflineFilesEnable
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - CscApi.dll
api_name:
 - OfflineFilesEnable
---

# OfflineFilesEnable function


## -description

Enables or disables the Offline Files feature.

## -parameters

### -param bEnable [in]

Specify <b>TRUE</b> to enable Offline Files, or <b>FALSE</b> to disable.

### -param pbRebootRequired [out]

Receives <b>TRUE</b> if a system restart is necessary to apply the desired configuration, or <b>FALSE</b> otherwise.

## -returns

Returns <b>ERROR_SUCCESS</b> if successful or a Win32 error value otherwise.

## -remarks

The Offline Files feature is implemented in two parts, the Offline Files service and the CSC driver.  When the  Offline Files feature is enabled, this means that the CSC driver's start type is set to SERVICE_SYSTEM_START and the Offline Files service's start type is set to SERVICE_AUTO_START.  If the driver is not already running, the caller must restart the computer after calling this method.

Disabling Offline Files disables both the service and the driver.  To disable the feature, the caller must restart the computer after calling this method.

The caller must be an administrator on the local computer.

