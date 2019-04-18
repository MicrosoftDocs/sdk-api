---
UID: NF:setupapi.SetupSetFileQueueAlternatePlatformW
title: SetupSetFileQueueAlternatePlatformW function (setupapi.h)
author: windows-sdk-content
description: The SetupSetFileQueueAlternatePlatform function associates the file queue with a target platform that is different from the platform running the function. This is done to enable for non-native signature verification.
old-location: setup\setupsetfilequeuealternateplatform.htm
tech.root: SetupApi
ms.assetid: 86289ab5-c313-470d-9ac1-3651c23af979
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: SetupSetFileQueueAlternatePlatform, SetupSetFileQueueAlternatePlatform function [Setup API], SetupSetFileQueueAlternatePlatformA, SetupSetFileQueueAlternatePlatformW, _setupapi_setupsetfilequeuealternateplatform, setup.setupsetfilequeuealternateplatform, setupapi/SetupSetFileQueueAlternatePlatform, setupapi/SetupSetFileQueueAlternatePlatformA, setupapi/SetupSetFileQueueAlternatePlatformW
ms.topic: function
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# SetupSetFileQueueAlternatePlatformW function


## -description


<p class="CCE_Message">[This function is available for use in the operating systems indicated in the Requirements section. It may be altered or unavailable in subsequent versions.   SetupAPI should no longer be used for installing applications. Instead, use the Windows Installer for developing application installers. SetupAPI continues to be used for installing device drivers.]

The 
<b>SetupSetFileQueueAlternatePlatform</b> function associates the file queue with a target platform that is different from the platform running the function. This is done to enable for non-native signature verification.


## -parameters




### -param QueueHandle [in]

Handle to an open setup file queue.


### -param AlternatePlatformInfo [in]

Optional pointer to an <a href="https://msdn.microsoft.com/33872a84-8f7f-4508-a326-2d95ac0fcfd7">SP_ALTPLATFORM_INFO</a> structure passing information about the alternate platform. On Windows 2000, the <b>cbSize</b> member of this structure must be set to sizeof(SP_ALTPLATFORM_INFO_V1). On Windows Server 2003 or Windows XP, the <b>cbSize</b> member of this structure must be set to sizeof(SP_ALTPLATFORM_INFO_V2).


### -param AlternateDefaultCatalogFile [in]

Pointer to a <b>null</b>-terminated string that specifies a catalog that validates any INF files. This parameter may be <b>NULL</b>.


## -returns



If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -see-also




<a href="https://msdn.microsoft.com/0a9518b7-f231-48f2-ba50-5b802f8ccaed">Functions</a>



<a href="https://msdn.microsoft.com/58201596-cb8c-480a-abef-896c1f9ef098">Overview</a>



<a href="https://msdn.microsoft.com/33872a84-8f7f-4508-a326-2d95ac0fcfd7">SP_ALTPLATFORM_INFO_V1</a>



<a href="https://msdn.microsoft.com/eb66ef5a-212d-4224-87b5-d64e8e188139">SP_ALTPLATFORM_INFO_V2</a>
 

 

