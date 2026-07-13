---
UID: NF:setupapi.SetupQueueRenameA
title: SetupQueueRenameA function (setupapi.h)
description: The SetupQueueRename function places an individual file rename operation on a setup file queue. (ANSI)
helpviewer_keywords: ["SetupQueueRenameA", "setupapi/SetupQueueRenameA"]
old-location: setup\setupqueuerename.htm
tech.root: setup
ms.assetid: 0b80eba9-9e71-4255-8c1b-039878682ec4
ms.date: 12/05/2018
ms.keywords: SetupQueueRename, SetupQueueRename function [Setup API], SetupQueueRenameA, SetupQueueRenameW, _setupapi_setupqueuerename, setup.setupqueuerename, setupapi/SetupQueueRename, setupapi/SetupQueueRenameA, setupapi/SetupQueueRenameW
req.header: setupapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SetupQueueRenameW (Unicode) and SetupQueueRenameA (ANSI)
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
 - SetupQueueRenameA
 - setupapi/SetupQueueRenameA
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
 - SetupQueueRename
 - SetupQueueRenameA
 - SetupQueueRenameW
---

# SetupQueueRenameA function


## -description

<p class="CCE_Message">[This function is available for use in the operating systems indicated in the Requirements section. It may be altered or unavailable in subsequent versions.   SetupAPI should no longer be used for installing applications. Instead, use the Windows Installer for developing application installers. SetupAPI continues to be used for installing device drivers.]

The 
<b>SetupQueueRename</b> function places an individual file rename operation on a setup file queue.

## -parameters

### -param QueueHandle [in]

Handle to a setup file queue, as returned by 
<a href="/windows/desktop/api/setupapi/nf-setupapi-setupopenfilequeue">SetupOpenFileQueue</a>.

### -param SourcePath [in]

Pointer to a null-terminated string that specifies the source path of the file to be renamed. If <i>SourceFileName</i> is not specified, <i>SourcePath</i> is assumed to be the full path.

### -param SourceFilename [in]

Pointer to a null-terminated string that specifies the file name part of the file to be renamed. If not specified, <i>SourcePath</i> is the full path.

### -param TargetPath [in]

Pointer to a null-terminated string that specifies the target directory. When this parameter is specified, the rename operation is actually a move operation. If <i>TargetPath</i> is not specified, the file is renamed but remains in its current location.

### -param TargetFilename [in]

Pointer to a null-terminated string that specifies the new name for the source file.

## -returns

If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

Because rename operations are assumed to take place on fixed media, the user will not be prompted when the queue is committed.





> [!NOTE]
> The setupapi.h header defines SetupQueueRename as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/SetupApi/functions">Functions</a>



<a href="/windows/desktop/SetupApi/overview">Overview</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupqueuecopya">SetupQueueCopy</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupqueuedeletea">SetupQueueDelete</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupqueuerenamesectiona">SetupQueueRenameSection</a>
