---
UID: NF:processenv.NeedCurrentDirectoryForExePathW
title: NeedCurrentDirectoryForExePathW function (processenv.h)
description: Determines whether the current directory should be included in the search path for the specified executable. (Unicode)
helpviewer_keywords: ["NeedCurrentDirectoryForExePath", "NeedCurrentDirectoryForExePath function", "NeedCurrentDirectoryForExePathW", "base.needcurrentdirectoryforexepath", "processenv/NeedCurrentDirectoryForExePath", "processenv/NeedCurrentDirectoryForExePathW"]
old-location: base\needcurrentdirectoryforexepath.htm
tech.root: backup
ms.assetid: 2bdc07b9-bb83-48c2-a668-fda5c69d54ee
ms.date: 12/05/2018
ms.keywords: NeedCurrentDirectoryForExePath, NeedCurrentDirectoryForExePath function, NeedCurrentDirectoryForExePathA, NeedCurrentDirectoryForExePathW, base.needcurrentdirectoryforexepath, processenv/NeedCurrentDirectoryForExePath, processenv/NeedCurrentDirectoryForExePathA, processenv/NeedCurrentDirectoryForExePathW, winbase/NeedCurrentDirectoryForExePath, winbase/NeedCurrentDirectoryForExePathA, winbase/NeedCurrentDirectoryForExePathW
req.header: processenv.h
req.include-header: Windows.h on Windows Vista, Windows 7, Windows Server 2008  Windows Server 2008 R2
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: NeedCurrentDirectoryForExePathW (Unicode) and NeedCurrentDirectoryForExePathA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - NeedCurrentDirectoryForExePathW
 - processenv/NeedCurrentDirectoryForExePathW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - API-MS-Win-Core-misc-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-ProcessEnvironment-l1-2-0.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
api_name:
 - NeedCurrentDirectoryForExePath
 - NeedCurrentDirectoryForExePathA
 - NeedCurrentDirectoryForExePathW
---

# NeedCurrentDirectoryForExePathW function


## -description

Determines whether the current directory should be included in the search path for the specified executable.

## -parameters

### -param ExeName [in]

The name of the executable file.

## -returns

If the current directory should be part of the search path, the return value is TRUE. Otherwise, the return value is FALSE.

## -remarks

This function should only be called in instances where the caller must explicitly resolve a relative executable name to an absolute name.  If <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa">CreateProcess</a> is called with a relative executable name, it will automatically search for the executable, calling  this function to determine the search path.

Most system functions perform their own path resolution, therefore, this function should only be called if you are attempting to resolve a search path for the specified executable based on the current directory.

The value of the NoDefaultCurrentDirectoryInExePath environment variable determines the value this function returns. However, you should call this function rather than checking the environment variable directly, as the registry location of this environment variable can change.

If the value of the <i>ExeName</i> parameter contains a backslash (\\), this function will always return TRUE. If it does not contain a backslash, the existence of the NoDefaultCurrentDirectoryInExePath environment variable is checked, and not its value.

An example of an instance when this function should be called instead of relying on the default search path resolution algorithm in <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa">CreateProcess</a> is the "cmd.exe" executable. It calls this function to determine the command search path because it does its own path resolution before calling <b>CreateProcess</b>.  If this function returns TRUE, cmd.exe uses the path ".;%PATH%" for the executable search. If it returns FALSE, cmd.exe uses the path "%PATH%" for the search.





> [!NOTE]
> The processenv.h header defines NeedCurrentDirectoryForExePath as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa">CreateProcess</a>



<a href="/windows/desktop/ProcThread/process-and-thread-functions">Process and Thread Functions</a>
