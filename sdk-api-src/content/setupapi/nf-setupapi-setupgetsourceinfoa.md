---
UID: NF:setupapi.SetupGetSourceInfoA
title: SetupGetSourceInfoA function (setupapi.h)
description: The SetupGetSourceInfo function retrieves the path, tag file, or media description for a source listed in an INF file. (ANSI)
helpviewer_keywords: ["SetupGetSourceInfoA", "setupapi/SetupGetSourceInfoA"]
old-location: setup\setupgetsourceinfo.htm
tech.root: setup
ms.assetid: 15bedd7f-7079-4623-a797-db308a51093f
ms.date: 12/05/2018
ms.keywords: SetupGetSourceInfo, SetupGetSourceInfo function [Setup API], SetupGetSourceInfoA, SetupGetSourceInfoW, _setupapi_setupgetsourceinfo, setup.setupgetsourceinfo, setupapi/SetupGetSourceInfo, setupapi/SetupGetSourceInfoA, setupapi/SetupGetSourceInfoW
req.header: setupapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SetupGetSourceInfoW (Unicode) and SetupGetSourceInfoA (ANSI)
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
 - SetupGetSourceInfoA
 - setupapi/SetupGetSourceInfoA
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
 - SetupGetSourceInfo
 - SetupGetSourceInfoA
 - SetupGetSourceInfoW
---

# SetupGetSourceInfoA function


## -description

<p class="CCE_Message">[This function is available for use in the operating systems indicated in the Requirements section. It may be altered or unavailable in subsequent versions.   SetupAPI should no longer be used for installing applications. Instead, use the Windows Installer for developing application installers. SetupAPI continues to be used for installing device drivers.]

The 
<b>SetupGetSourceInfo</b> function retrieves the path, tag file, or media description for a source listed in an INF file.

## -parameters

### -param InfHandle [in]

Handle to an open INF file that contains a <b>SourceDisksNames</b> section. If platform-specific sections exist for the user's system (for example, <b>SourceDisksNames.x86</b>), the platform-specific section will be used.

### -param SourceId [in]

Identifier for a source media. This value is used to search by key in the <b>SourceDisksNames</b> section.

### -param InfoDesired [in]

Indicates what information is desired. Only one value may be specified per function call, and they cannot be combined. The following types of information can be retrieved from a <b>SourceDisksNames</b> section. 







#### SRCINFO_PATH

The path specified for the source. This is not a full path, but the path relative to the installation root.



#### SRCINFO_TAGFILE

The tag file that identifies the source media, or if cabinets are used, the name of the cabinet file.



#### SRCINFO_DESCRIPTION

A description for the media.

### -param ReturnBuffer [in, out]

Optional pointer to a buffer to receive the retrieved information.  Path returns are guaranteed not to end with \.  You should use a <b>null</b>-terminated string. The <b>null</b>-terminated string should not exceed the size of the destination buffer. You can call the function once to get the required buffer size, allocate the necessary memory, and then call the function a second time to retrieve the data. See the Remarks section. Using this technique, you can avoid errors due to an insufficient buffer size. This parameter can be <b>NULL</b>.

### -param ReturnBufferSize [in]

Size of the buffer pointed to by <i>ReturnBuffer</i>, in characters. This  includes the <b>null</b> terminator.

### -param RequiredSize [in, out]

Optional pointer to a variable that receives the required size for the buffer specified by <i>ReturnBuffer</i>, in characters. This includes the <b>null</b> terminator. If <i>ReturnBuffer</i> is specified and the actual size needed is larger than the value specified by <i>ReturnBufferSize</i>, the function fails and a call to <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> returns ERROR_INSUFFICIENT_BUFFER.

## -returns

If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

If this function is called with a <i>ReturnBuffer</i> of <b>NULL</b> and a <i>ReturnBufferSize</i> of zero, the function puts the buffer size needed to hold the specified data into the variable pointed to by <i>RequiredSize</i>. If the function succeeds in this, the return value is a nonzero value. Otherwise, the return value is zero and extended error information can be obtained by calling <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.






> [!NOTE]
> The setupapi.h header defines SetupGetSourceInfo as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/SetupApi/functions">Functions</a>



<a href="/windows/desktop/SetupApi/overview">Overview</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupgetsourcefilelocationa">SetupGetSourceFileLocation</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupgetsourcefilesizea">SetupGetSourceFileSize</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupgettargetpatha">SetupGetTargetPath</a>
