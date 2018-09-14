---
UID: NF:srpapi.SrpDisablePermissiveModeFileEncryption
title: SrpDisablePermissiveModeFileEncryption function
author: windows-sdk-content
description: Disables permissive mode for file encryption on the current thread.
old-location: edp\srpdisablepermissivemodefileencryption_.htm
tech.root: EDP
ms.assetid: CB75BAFE-EB2A-43F2-8689-34E798C3B9F5
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: EDP.srpdisablepermissivemodefileencryption_, SrpDisablePermissiveModeFileEncryption, SrpDisablePermissiveModeFileEncryption , SrpDisablePermissiveModeFileEncryption function, srpapi/SrpDisablePermissiveModeFileEncryption
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
 - SrpDisablePermissiveModeFileEncryption
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SrpDisablePermissiveModeFileEncryption function


## -description



<div class="alert"><b>Note</b>  Windows Information Protection (WIP) policy can be applied on Windows 10, version 1607.</div>
<div> </div>Disables permissive mode for file encryption on the current thread. 

Use <a href="https://msdn.microsoft.com/4CC6D174-55FC-40D7-BE7B-5F56B27DA225">SrpEnablePermissiveModeFileEncryption</a> to enable the mode. 

This API does not attempt to handle nested calls by reference counting or such. The first call to <b>SrpDisablePermissiveModeFileEncryption</b> will disable the permissive mode.


## -parameters






## -returns



If this function succeeds, it returns S_OK. 

HRESULT_FROM_WIN32 (ERROR_INVALID_STATE) indicates that thread tagging cannot be performed due to either process or thread context.



