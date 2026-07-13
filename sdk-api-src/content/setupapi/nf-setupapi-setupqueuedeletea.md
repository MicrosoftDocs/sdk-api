---
UID: NF:setupapi.SetupQueueDeleteA
title: SetupQueueDeleteA function (setupapi.h)
description: The SetupQueueDelete function places an individual file delete operation on a setup file queue. (ANSI)
helpviewer_keywords: ["SetupQueueDeleteA", "setupapi/SetupQueueDeleteA"]
old-location: setup\setupqueuedelete.htm
tech.root: setup
ms.assetid: 21cdaf05-c4fb-4130-baa5-31baf5391ece
ms.date: 12/05/2018
ms.keywords: SetupQueueDelete, SetupQueueDelete function [Setup API], SetupQueueDeleteA, SetupQueueDeleteW, _setupapi_setupqueuedelete, setup.setupqueuedelete, setupapi/SetupQueueDelete, setupapi/SetupQueueDeleteA, setupapi/SetupQueueDeleteW
req.header: setupapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SetupQueueDeleteW (Unicode) and SetupQueueDeleteA (ANSI)
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
 - SetupQueueDeleteA
 - setupapi/SetupQueueDeleteA
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
 - SetupQueueDelete
 - SetupQueueDeleteA
 - SetupQueueDeleteW
---

# SetupQueueDeleteA function


## -description

<p class="CCE_Message">[This function is available for use in the operating systems indicated in the Requirements section. It may be altered or unavailable in subsequent versions.   SetupAPI should no longer be used for installing applications. Instead, use the Windows Installer for developing application installers. SetupAPI continues to be used for installing device drivers.]

The 
<b>SetupQueueDelete</b> function places an individual file delete operation on a setup file queue.

## -parameters

### -param QueueHandle [in]

Handle to a setup file queue, as returned by 
<a href="/windows/desktop/api/setupapi/nf-setupapi-setupopenfilequeue">SetupOpenFileQueue</a>.

### -param PathPart1 [in]

Pointer to a <b>null</b>-terminated string that specifies the first part of the path of the file to be deleted. If <i>PathPart2</i> is <b>NULL</b>, <i>PathPart1</i> is the full path of the file to be deleted.

### -param PathPart2 [in]

Pointer to a <b>null</b>-terminated string that specifies the second part of the path of the file to be deleted. This parameter may be <b>NULL</b>. This is appended to <i>PathPart1</i> to form the full path of the file to be deleted. The function checks for and collapses duplicated path separators when it combines <i>PathPart1</i> and <i>PathPart2</i>.

## -returns

If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

Because delete operations are assumed to take place on fixed media, the user will not be prompted when the queue is committed.





> [!NOTE]
> The setupapi.h header defines SetupQueueDelete as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/SetupApi/functions">Functions</a>



<a href="/windows/desktop/SetupApi/overview">Overview</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupqueuecopya">SetupQueueCopy</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupqueuedeletesectiona">SetupQueueDeleteSection</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupqueuerenamea">SetupQueueRename</a>
