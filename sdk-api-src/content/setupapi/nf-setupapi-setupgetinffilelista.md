---
UID: NF:setupapi.SetupGetInfFileListA
title: SetupGetInfFileListA function (setupapi.h)
description: The SetupGetInfFileList function returns a list of INF files located in a caller-specified directory to a call-supplied buffer. (ANSI)
helpviewer_keywords: ["SetupGetInfFileListA", "setupapi/SetupGetInfFileListA"]
old-location: setup\setupgetinffilelist.htm
tech.root: setup
ms.assetid: d7074e88-757c-4ca9-adaf-2010472f106c
ms.date: 12/05/2018
ms.keywords: SetupGetInfFileList, SetupGetInfFileList function [Setup API], SetupGetInfFileListA, SetupGetInfFileListW, _setupapi_setupgetinffilelist, setup.setupgetinffilelist, setupapi/SetupGetInfFileList, setupapi/SetupGetInfFileListA, setupapi/SetupGetInfFileListW
req.header: setupapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SetupGetInfFileListW (Unicode) and SetupGetInfFileListA (ANSI)
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
 - SetupGetInfFileListA
 - setupapi/SetupGetInfFileListA
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
 - SetupGetInfFileList
 - SetupGetInfFileListA
 - SetupGetInfFileListW
---

# SetupGetInfFileListA function


## -description

<p class="CCE_Message">[This function is available for use in the operating systems indicated in the Requirements section. It may be altered or unavailable in subsequent versions.   SetupAPI should no longer be used for installing applications. Instead, use the Windows Installer for developing application installers. SetupAPI continues to be used for installing device drivers.]

The 
<b>SetupGetInfFileList</b> function returns a list of INF files located in a caller-specified directory to a call-supplied buffer.

## -parameters

### -param DirectoryPath [in]

Optional pointer to a <b>null</b>-terminated string containing the path of the directory in which to search. If this value is <b>NULL</b>, the %windir%\inf directory is used.

### -param InfStyle [in]

Type of INF file to search for. May be a combination of the following flags. 







#### INF_STYLE_OLDNT

A legacy INF file format.



#### INF_STYLE_WIN4

A Windows INF file format.

### -param ReturnBuffer [in, out]

 If not <b>NULL</b>, points to a buffer in which this function returns the list of all INF files of the desired styles that were found in the specified subdirectory. File names are <b>null</b>-terminated, with an extra <b>null</b> at the end of the list. The <b>null</b>-terminated string should not exceed the size of the destination buffer. You can call the function once to get the required buffer size, allocate the necessary memory, and then call the function a second time to retrieve the data. Using this technique, you can avoid errors due to an insufficient buffer size. The filenames do not include the path. See the Remarks section.

### -param ReturnBufferSize [in]

Size of the buffer pointed to by the <i>ReturnBuffer</i> parameter, in characters. This includes the <b>null</b> terminator. If <i>ReturnBuffer</i> is not specified, <i>ReturnBufferSize</i> is ignored.

### -param RequiredSize [in, out]

If not <b>NULL</b>, points to a variable in which this function returns the required size for the buffer pointed to by the <i>ReturnBuffer</i> parameter, in characters. This includes the <b>null</b> terminator. If <i>ReturnBuffer</i> is specified and the size needed is larger than <i>ReturnBufferSize</i>, the function fails and a call to <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> returns ERROR_INSUFFICIENT_BUFFER.

## -returns

If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

If this function is called with a ReturnBuffer of <b>NULL</b> and a <i>ReturnBufferSize</i> of zero, the function puts the buffer size needed to hold the specified data into the variable pointed to by <i>RequiredSize</i>. If the function succeeds in this, the return value is a nonzero value. Otherwise, the return value is zero and extended error information can be obtained by calling <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.


If multiple INF file styles are returned by this function, the style of a particular INF file can be determined by calling the <a href="/windows/desktop/api/setupapi/nf-setupapi-setupgetinfinformationa">SetupGetInfInformation</a> function





> [!NOTE]
> The setupapi.h header defines SetupGetInfFileList as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/SetupApi/functions">Functions</a>



<a href="/windows/desktop/SetupApi/overview">Overview</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupgetinfinformationa">SetupGetInfInformation</a>
