---
UID: NF:setupapi.SetupGetTargetPathA
title: SetupGetTargetPathA function (setupapi.h)
description: The SetupGetTargetPath function determines the target directory for a file list section. (ANSI)
helpviewer_keywords: ["SetupGetTargetPathA", "setupapi/SetupGetTargetPathA"]
old-location: setup\setupgettargetpath.htm
tech.root: setup
ms.assetid: fe98f00e-7887-4e37-8e09-037a804e6195
ms.date: 12/05/2018
ms.keywords: SetupGetTargetPath, SetupGetTargetPath function [Setup API], SetupGetTargetPathA, SetupGetTargetPathW, _setupapi_setupgettargetpath, setup.setupgettargetpath, setupapi/SetupGetTargetPath, setupapi/SetupGetTargetPathA, setupapi/SetupGetTargetPathW
req.header: setupapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SetupGetTargetPathW (Unicode) and SetupGetTargetPathA (ANSI)
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
 - SetupGetTargetPathA
 - setupapi/SetupGetTargetPathA
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
 - SetupGetTargetPath
 - SetupGetTargetPathA
 - SetupGetTargetPathW
---

# SetupGetTargetPathA function


## -description

<p class="CCE_Message">[This function is available for use in the operating systems indicated in the Requirements section. It may be altered or unavailable in subsequent versions.   SetupAPI should no longer be used for installing applications. Instead, use the Windows Installer for developing application installers. SetupAPI continues to be used for installing device drivers.]

The 
<b>SetupGetTargetPath</b> function determines the target directory for a file list section. The file list section can be a <b>Copy Files</b> section, a <b>Delete Files</b> section, or a <b>Rename Files</b> section. All the files in the section must be in a single directory that is listed in a <b>DestinationDirs</b> section of the INF file.

## -parameters

### -param InfHandle [in]

Handle to the load INF file that contains a <b>DestinationDirs</b> section.

### -param InfContext [in]

Optional pointer to an INF context that specifies a line in a file list section whose destination directory is to be retrieved. If <i>InfContext</i> is <b>NULL</b>, then the <i>Section</i> parameter is used.

### -param Section [in]

Optional parameter that specifies the name of a section of the INF file whose handle is <i>InfHandle</i>. 
<b>SetupGetTargetPath</b> retrieves the target directory for this section. The <i>Section</i> parameter is ignored if <i>InfContext</i> is specified. If neither <i>InfContext</i> nor <i>Section</i> is specified, the function retrieves the default target path from the INF file. You should use a <b>null</b>-terminated string.

### -param ReturnBuffer [in, out]

Optional pointer to  buffer to receive the fully qualified  target path. The path is guaranteed not to end with \. You should use a <b>null</b>-terminated string. You can call the function once to get the required buffer size, allocate the necessary memory, and then call the function a second time to retrieve the data. Using this technique, you can avoid errors due to an insufficient buffer size. See the Remarks section. This parameter can be <b>NULL</b>.

### -param ReturnBufferSize [in]

Size of the buffer pointed to by <i>ReturnBuffer</i>, in characters. This includes the <b>null</b> terminator.

### -param RequiredSize [in, out]

Optional pointer to a  variable that receives the required size for the buffer pointed to by <i>ReturnBuffer</i>, in characters. This includes the <b>null</b> terminator.  If the actual size needed is larger than the value specified by <i>ReturnBufferSize</i>, the function fails and a call to <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> returns ERROR_INSUFFICIENT_BUFFER.

## -returns

If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

If this function is called with a <i>ReturnBuffer</i> of <b>NULL</b> and a <i>ReturnBufferSize</i> of zero, the function puts the buffer size needed to hold the specified data into the variable pointed to by <i>RequiredSize</i>. If the function succeeds in this, the return value is a nonzero value. Otherwise, the return value is zero and extended error information can be obtained by calling <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.





> [!NOTE]
> The setupapi.h header defines SetupGetTargetPath as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/SetupApi/functions">Functions</a>



<a href="/windows/desktop/SetupApi/overview">Overview</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupgetsourcefilelocationa">SetupGetSourceFileLocation</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupgetsourcefilesizea">SetupGetSourceFileSize</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupgetsourceinfoa">SetupGetSourceInfo</a>
