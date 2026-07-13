---
UID: NF:setupapi.SetupQueueDeleteSectionW
title: SetupQueueDeleteSectionW function (setupapi.h)
description: The SetupQueueDeleteSection function queues all the files in a section of an INF file for deletion. The section must be in the correct Delete Files format and the INF file must contain a DestinationDirs section. (Unicode)
helpviewer_keywords: ["SetupQueueDeleteSection", "SetupQueueDeleteSection function [Setup API]", "SetupQueueDeleteSectionW", "_setupapi_setupqueuedeletesection", "setup.setupqueuedeletesection", "setupapi/SetupQueueDeleteSection", "setupapi/SetupQueueDeleteSectionW"]
old-location: setup\setupqueuedeletesection.htm
tech.root: setup
ms.assetid: 3e76e345-1d6c-4eb5-a743-b71d5ccc52e5
ms.date: 12/05/2018
ms.keywords: SetupQueueDeleteSection, SetupQueueDeleteSection function [Setup API], SetupQueueDeleteSectionA, SetupQueueDeleteSectionW, _setupapi_setupqueuedeletesection, setup.setupqueuedeletesection, setupapi/SetupQueueDeleteSection, setupapi/SetupQueueDeleteSectionA, setupapi/SetupQueueDeleteSectionW
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SetupQueueDeleteSectionW
 - setupapi/SetupQueueDeleteSectionW
dev_langs:
 - c++
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
---

# SetupQueueDeleteSectionW function


## -description

<p class="CCE_Message">[This function is available for use in the operating systems indicated in the Requirements section. It may be altered or unavailable in subsequent versions.   SetupAPI should no longer be used for installing applications. Instead, use the Windows Installer for developing application installers. SetupAPI continues to be used for installing device drivers.]

The 
<b>SetupQueueDeleteSection</b> function queues all the files in a section of an INF file for deletion. The section must be in the correct <b>Delete Files</b> format and the INF file must contain a <b>DestinationDirs</b> section.

## -parameters

### -param QueueHandle [in]

Handle to a setup file queue, as returned by 
<a href="/windows/desktop/api/setupapi/nf-setupapi-setupopenfilequeue">SetupOpenFileQueue</a>.

### -param InfHandle [in]

Handle to an open INF file that contains the <b>DestinationDirs</b> section. If <i>ListInfHandle</i> is not specified, <i>InfHandle</i> contains the section name.

### -param ListInfHandle [in]

Optional  handle to an open INF file that contains the section to queue for deletion. If <i>ListInfHandle</i> is not specified, <i>InfHandle</i> is assumed to contain the section name.

### -param Section [in]

Pointer to a  null-terminated string that specifies the name of the section to be queued for deletion.

## -returns

If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

This function requires a Windows INF file. Some older INF file  formats may not be supported. 





> [!NOTE]
> The setupapi.h header defines SetupQueueDeleteSection as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/SetupApi/functions">Functions</a>



<a href="/windows/desktop/SetupApi/overview">Overview</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupqueuecopysectiona">SetupQueueCopySection</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupqueuedeletea">SetupQueueDelete</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupqueuerenamesectiona">SetupQueueRenameSection</a>
