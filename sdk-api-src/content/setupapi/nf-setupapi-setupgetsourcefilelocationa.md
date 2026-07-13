---
UID: NF:setupapi.SetupGetSourceFileLocationA
title: SetupGetSourceFileLocationA function (setupapi.h)
description: The SetupGetSourceFileLocation function retrieves the location of a source file listed in an INF file. (ANSI)
helpviewer_keywords: ["SetupGetSourceFileLocationA", "setupapi/SetupGetSourceFileLocationA"]
old-location: setup\setupgetsourcefilelocation.htm
tech.root: setup
ms.assetid: 00245cb9-99de-464a-a0b4-d1efb1f1331b
ms.date: 12/05/2018
ms.keywords: SetupGetSourceFileLocation, SetupGetSourceFileLocation function [Setup API], SetupGetSourceFileLocationA, SetupGetSourceFileLocationW, _setupapi_setupgetsourcefilelocation, setup.setupgetsourcefilelocation, setupapi/SetupGetSourceFileLocation, setupapi/SetupGetSourceFileLocationA, setupapi/SetupGetSourceFileLocationW
req.header: setupapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SetupGetSourceFileLocationW (Unicode) and SetupGetSourceFileLocationA (ANSI)
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
 - SetupGetSourceFileLocationA
 - setupapi/SetupGetSourceFileLocationA
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
 - SetupGetSourceFileLocation
 - SetupGetSourceFileLocationA
 - SetupGetSourceFileLocationW
---

# SetupGetSourceFileLocationA function


## -description

<p class="CCE_Message">[This function is available for use in the operating systems indicated in the Requirements section. It may be altered or unavailable in subsequent versions.   SetupAPI should no longer be used for installing applications. Instead, use the Windows Installer for developing application installers. SetupAPI continues to be used for installing device drivers.]

The 
<b>SetupGetSourceFileLocation</b> function retrieves the location of a source file listed in an INF file.

## -parameters

### -param InfHandle [in]

Handle to the INF file that contains the <b>SourceDisksNames</b> and <b>SourceDisksFiles</b> sections. If platform-specific sections exist for the user's system (for example, <b>SourceDisksNames.x86</b> and <b>SourceDisksFiles.x86</b>), the platform-specific section will be used.

### -param InfContext [in]

Optional pointer to the context of a line in a <b>Copy Files</b> section for which the full source path is to be retrieved. If this parameter is <b>NULL</b>, <i>FileName</i> is searched for in the <b>SourceDisksFiles</b> section of the INF file specified by <i>InfHandle</i>.

### -param FileName [in]

Optional pointer to a <b>null</b>-terminated string containing the filename (no path) for which to return the full source location. This parameter can be <b>NULL</b>, but either <i>FileName</i> or <i>InfContext</i> must be specified.

### -param SourceId [in, out]

Pointer to a variable that receives the source identifier of the media where the file is located from the <b>SourceDisksNames</b> section of the INF file.

### -param ReturnBuffer [in, out]

 Optional pointer to a buffer to receive the relative source path. The source path does not include the filename itself, nor does it include a drive letter/network share name. The path does not start or end with a backslash (\), so the empty string specifies the root directory. You should use a <b>null</b>-terminated string buffer. The <b>null</b>-terminated string should not exceed the size of the destination buffer. You can call the function once to get the required buffer size, allocate the necessary memory, and then call the function a second time to retrieve the data.  Using this technique, you can avoid errors due to an insufficient buffer size. See the Remarks section. This parameter can be <b>NULL</b>.

### -param ReturnBufferSize [out]

Size of the buffer pointed to by <i>ReturnBuffer</i>, in characters. This number includes the <b>null</b> terminator.

### -param RequiredSize [in, out]

Optional pointer to a variable that receives the required size for the buffer pointed to by the <i>ReturnBuffer</i> parameter, in characters. This number includes the <b>null</b> terminator. If the required size is larger than the value specified by <i>ReturnBufferSize</i>, the function fails and <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> returns ERROR_INSUFFICIENT_BUFFER.

## -returns

If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

If this function is called with a <i>ReturnBuffer</i> of <b>NULL</b> and a <i>ReturnBufferSize</i> of zero, the function puts the buffer size needed to hold the specified data into the variable pointed to by <i>RequiredSize</i>. If the function succeeds in this, the return value is a nonzero value. Otherwise, the return value is zero and extended error information can be obtained by calling <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.





> [!NOTE]
> The setupapi.h header defines SetupGetSourceFileLocation as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/SetupApi/functions">Functions</a>



<a href="/windows/desktop/SetupApi/overview">Overview</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupgetsourcefilesizea">SetupGetSourceFileSize</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupgetsourceinfoa">SetupGetSourceInfo</a>
