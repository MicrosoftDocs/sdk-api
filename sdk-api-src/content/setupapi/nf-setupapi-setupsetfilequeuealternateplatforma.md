---
UID: NF:setupapi.SetupSetFileQueueAlternatePlatformA
title: SetupSetFileQueueAlternatePlatformA function (setupapi.h)
description: The SetupSetFileQueueAlternatePlatform function associates the file queue with a target platform that is different from the platform running the function. This is done to enable for non-native signature verification.
old-location: setup\setupsetfilequeuealternateplatform.htm
tech.root: SetupApi
ms.assetid: 86289ab5-c313-470d-9ac1-3651c23af979
ms.date: 12/05/2018
ms.keywords: SetupSetFileQueueAlternatePlatform, SetupSetFileQueueAlternatePlatform function [Setup API], SetupSetFileQueueAlternatePlatformA, SetupSetFileQueueAlternatePlatformW, _setupapi_setupsetfilequeuealternateplatform, setup.setupsetfilequeuealternateplatform, setupapi/SetupSetFileQueueAlternatePlatform, setupapi/SetupSetFileQueueAlternatePlatformA, setupapi/SetupSetFileQueueAlternatePlatformW
f1_keywords:
- setupapi/SetupSetFileQueueAlternatePlatform
dev_langs:
- c++
req.header: setupapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SetupSetFileQueueAlternatePlatformW (Unicode) and SetupSetFileQueueAlternatePlatformA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Setupapi.lib
req.dll: Setupapi.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- Setupapi.dll
api_name:
- SetupSetFileQueueAlternatePlatform
- SetupSetFileQueueAlternatePlatformA
- SetupSetFileQueueAlternatePlatformW
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# SetupSetFileQueueAlternatePlatformA function


## -description


<p class="CCE_Message">[This function is available for use in the operating systems indicated in the Requirements section. It may be altered or unavailable in subsequent versions.   SetupAPI should no longer be used for installing applications. Instead, use the Windows Installer for developing application installers. SetupAPI continues to be used for installing device drivers.]

The 
<b>SetupSetFileQueueAlternatePlatform</b> function associates the file queue with a target platform that is different from the platform running the function. This is done to enable for non-native signature verification.


## -parameters




### -param QueueHandle [in]

Handle to an open setup file queue.


### -param AlternatePlatformInfo [in]

Optional pointer to an <a href="https://docs.microsoft.com/windows/desktop/api/setupapi/ns-setupapi-sp_altplatform_info_v1">SP_ALTPLATFORM_INFO</a> structure passing information about the alternate platform. On Windows 2000, the <b>cbSize</b> member of this structure must be set to sizeof(SP_ALTPLATFORM_INFO_V1). On Windows Server 2003 or Windows XP, the <b>cbSize</b> member of this structure must be set to sizeof(SP_ALTPLATFORM_INFO_V2).


### -param AlternateDefaultCatalogFile [in]

Pointer to a <b>null</b>-terminated string that specifies a catalog that validates any INF files. This parameter may be <b>NULL</b>.


## -returns



If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/SetupApi/functions">Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/SetupApi/overview">Overview</a>



<a href="https://docs.microsoft.com/windows/desktop/api/setupapi/ns-setupapi-sp_altplatform_info_v1">SP_ALTPLATFORM_INFO_V1</a>



<a href="https://docs.microsoft.com/windows/desktop/api/setupapi/ns-setupapi-sp_altplatform_info_v2">SP_ALTPLATFORM_INFO_V2</a>
 

 

