---
UID: NF:setupapi.SetupQueueDeleteSectionA
title: SetupQueueDeleteSectionA function (setupapi.h)
description: The SetupQueueDeleteSection function queues all the files in a section of an INF file for deletion. The section must be in the correct Delete Files format and the INF file must contain a DestinationDirs section.helpviewer_keywords: ["SetupQueueDeleteSection","SetupQueueDeleteSection function [Setup API]","SetupQueueDeleteSectionA","SetupQueueDeleteSectionW","_setupapi_setupqueuedeletesection","setup.setupqueuedeletesection","setupapi/SetupQueueDeleteSection","setupapi/SetupQueueDeleteSectionA","setupapi/SetupQueueDeleteSectionW"]
old-location: setup\setupqueuedeletesection.htm
tech.root: SetupApi
ms.assetid: 3e76e345-1d6c-4eb5-a743-b71d5ccc52e5
ms.date: 12/05/2018
ms.keywords: SetupQueueDeleteSection, SetupQueueDeleteSection function [Setup API], SetupQueueDeleteSectionA, SetupQueueDeleteSectionW, _setupapi_setupqueuedeletesection, setup.setupqueuedeletesection, setupapi/SetupQueueDeleteSection, setupapi/SetupQueueDeleteSectionA, setupapi/SetupQueueDeleteSectionW
f1_keywords:
- setupapi/SetupQueueDeleteSection
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
req.unicode-ansi: SetupQueueDeleteSectionW (Unicode) and SetupQueueDeleteSectionA (ANSI)
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
- SetupQueueDeleteSection
- SetupQueueDeleteSectionA
- SetupQueueDeleteSectionW
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# SetupQueueDeleteSectionA function


## -description


<p class="CCE_Message">[This function is available for use in the operating systems indicated in the Requirements section. It may be altered or unavailable in subsequent versions.   SetupAPI should no longer be used for installing applications. Instead, use the Windows Installer for developing application installers. SetupAPI continues to be used for installing device drivers.]

The 
<b>SetupQueueDeleteSection</b> function queues all the files in a section of an INF file for deletion. The section must be in the correct <b>Delete Files</b> format and the INF file must contain a <b>DestinationDirs</b> section.


## -parameters




### -param QueueHandle [in]

Handle to a setup file queue, as returned by 
<a href="https://docs.microsoft.com/windows/desktop/api/setupapi/nf-setupapi-setupopenfilequeue">SetupOpenFileQueue</a>.


### -param InfHandle [in]

Handle to an open INF file that contains the <b>DestinationDirs</b> section. If <i>ListInfHandle</i> is not specified, <i>InfHandle</i> contains the section name. 


### -param ListInfHandle [in]

Optional  handle to an open INF file that contains the section to queue for deletion. If <i>ListInfHandle</i> is not specified, <i>InfHandle</i> is assumed to contain the section name.


### -param Section [in]

Pointer to a  null-terminated string that specifies the name of the section to be queued for deletion.


## -returns



If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.




## -remarks



This function requires a Windows INF file. Some older INF file  formats may not be supported. 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/SetupApi/functions">Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/SetupApi/overview">Overview</a>



<a href="https://docs.microsoft.com/windows/desktop/api/setupapi/nf-setupapi-setupqueuecopysectiona">SetupQueueCopySection</a>



<a href="https://docs.microsoft.com/windows/desktop/api/setupapi/nf-setupapi-setupqueuedeletea">SetupQueueDelete</a>



<a href="https://docs.microsoft.com/windows/desktop/api/setupapi/nf-setupapi-setupqueuerenamesectiona">SetupQueueRenameSection</a>
 

 

