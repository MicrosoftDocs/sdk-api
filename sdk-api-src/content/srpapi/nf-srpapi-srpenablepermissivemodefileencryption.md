---
UID: NF:srpapi.SrpEnablePermissiveModeFileEncryption
title: SrpEnablePermissiveModeFileEncryption function (srpapi.h)
description: Enables permissive mode for file encryption on the current thread and all threads this thread will create or post work to.
helpviewer_keywords: ["EDP.srpenablepermissivemodefileencryption_","SrpEnablePermissiveModeFileEncryption","SrpEnablePermissiveModeFileEncryption","SrpEnablePermissiveModeFileEncryption function","srpapi/SrpEnablePermissiveModeFileEncryption"]
old-location: edp\srpenablepermissivemodefileencryption_.htm
tech.root: EDP
ms.assetid: 4CC6D174-55FC-40D7-BE7B-5F56B27DA225
ms.date: 12/05/2018
ms.keywords: EDP.srpenablepermissivemodefileencryption_, SrpEnablePermissiveModeFileEncryption, SrpEnablePermissiveModeFileEncryption , SrpEnablePermissiveModeFileEncryption function, srpapi/SrpEnablePermissiveModeFileEncryption
req.header: srpapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Srpapi.lib
req.dll: Srpapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SrpEnablePermissiveModeFileEncryption
 - srpapi/SrpEnablePermissiveModeFileEncryption
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - srpapi.dll
 - Ext-MS-Win-Security-Srp-L1-1-0.dll
 - Ext-MS-Win-Security-Srp-L1-1-1.dll
api_name:
 - SrpEnablePermissiveModeFileEncryption
---

# SrpEnablePermissiveModeFileEncryption function


## -description

<div class="alert"><b>Note</b>  Windows Information Protection (WIP) policy can be applied on Windows 10, version 1607.</div>
<div> </div>Enables permissive mode for file encryption on the current thread and all threads this thread will create or post work to.

Use <a href="/previous-versions/windows/desktop/api/srpapi/nf-srpapi-srpdisablepermissivemodefileencryption">SrpDisablePermissiveModeFileEncryption</a> to disable the mode. 

This API does not attempt to handle nested calls by reference counting or such. Subsequent calls to <b>SrpEnablePermissiveModeFileEncryption</b> after the first successful call to this API will not have any effect.

## -parameters

### -param enterpriseId [in, optional]

Contains enterprise ID string. In TH2 this is not used.

## -returns

If this function succeeds, it returns S_OK. 

HRESULT_FROM_WIN32 (ERROR_INVALID_STATE) indicates that thread tagging cannot be performed due to either process or thread context.