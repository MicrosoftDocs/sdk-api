---
UID: NF:setupapi.SetupInstallFileA
title: SetupInstallFileA function (setupapi.h)
description: The SetupInstallFile function installs a file as specified either by an INFCONTEXT returned by SetupFindXXXLine or explicitly by the file name and path. (ANSI)
helpviewer_keywords: ["SP_COPY_DELETESOURCE", "SP_COPY_FORCE_IN_USE", "SP_COPY_FORCE_NEWER", "SP_COPY_FORCE_NOOVERWRITE", "SP_COPY_LANGUAGEAWARE", "SP_COPY_NEWER_ONLY", "SP_COPY_NEWER_OR_SAME", "SP_COPY_NODECOMP", "SP_COPY_NOOVERWRITE", "SP_COPY_REPLACEONLY", "SP_COPY_SOURCEPATH_ABSOLUTE", "SP_COPY_SOURCE_ABSOLUTE", "SetupInstallFileA", "setupapi/SetupInstallFileA"]
old-location: setup\setupinstallfile.htm
tech.root: setup
ms.assetid: 04db1553-1c9a-414e-a2b8-b087dd44ef55
ms.date: 12/05/2018
ms.keywords: SP_COPY_DELETESOURCE, SP_COPY_FORCE_IN_USE, SP_COPY_FORCE_NEWER, SP_COPY_FORCE_NOOVERWRITE, SP_COPY_LANGUAGEAWARE, SP_COPY_NEWER_ONLY, SP_COPY_NEWER_OR_SAME, SP_COPY_NODECOMP, SP_COPY_NOOVERWRITE, SP_COPY_REPLACEONLY, SP_COPY_SOURCEPATH_ABSOLUTE, SP_COPY_SOURCE_ABSOLUTE, SetupInstallFile, SetupInstallFile function [Setup API], SetupInstallFileA, SetupInstallFileW, _setupapi_setupinstallfile, setup.setupinstallfile, setupapi/SetupInstallFile, setupapi/SetupInstallFileA, setupapi/SetupInstallFileW
req.header: setupapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SetupInstallFileW (Unicode) and SetupInstallFileA (ANSI)
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
 - SetupInstallFileA
 - setupapi/SetupInstallFileA
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
 - SetupInstallFile
 - SetupInstallFileA
 - SetupInstallFileW
---

# SetupInstallFileA function


## -description

<p class="CCE_Message">[This function is available for use in the operating systems indicated in the Requirements section. It may be altered or unavailable in subsequent versions.   SetupAPI should no longer be used for installing applications. Instead, use the Windows Installer for developing application installers. SetupAPI continues to be used for installing device drivers.]

The 
<b>SetupInstallFile</b> function installs a file as specified either by an 
<a href="/windows/desktop/api/setupapi/ns-setupapi-infcontext">INFCONTEXT</a> returned by SetupFindXXXLine or explicitly by  the file name and path.

If a file is copied, the caller of this function must have write privileges into the target directory.

## -parameters

### -param InfHandle [in]

Optional pointer to the handle to an INF file that contains SourceDisksNames and SourceDisksFiles sections. If platform-specific sections exist for the user's system (for example, SourceDisksNames.x86 and SourceDisksFiles.x86), the platform-specific section will be used. If <i>InfContext</i> is null and <i>CopyStyle</i> includes SP_COPY_SOURCE_ABSOLUTE or SP_COPY_SOURCEPATH_ABSOLUTE, <i>InfHandle</i> is ignored.

### -param InfContext [in]

Optional pointer to the context of a line in a Copy Files section in an INF file. The routine looks up this file  in the SourceDisksFiles section of <i>InfHandle</i> to get file copy information. If <i>InfHandle</i> is not specified, <i>SourceFile</i> must be.

### -param SourceFile [in]

Optional pointer to the file name (no path) of the file to copy. The file is looked up in the SourceDisksFiles section. The <i>SourceFile</i> parameter must be specified if <i>InfContext</i> is not. <i>SourceFile</i> is ignored if <i>InfContext</i> is specified.

### -param SourcePathRoot [in]

Optional pointer to the root path for the file to be copied (for example, A:\ or F:\). Paths in the SourceDisksNames section are appended to this path. The <i>SourcePathRoot</i> parameter is ignored if <i>CopyStyle</i> includes the SP_COPY_SOURCE_ABSOLUTE flag.

### -param DestinationName [in]

Optional pointer to the file name only (no path) of the target file. This parameter can be null to indicate that the target file should have the same name as the source file. If <i>InfContext</i> is not specified, <i>DestinationName</i> supplies the full  path and file name for the target.

### -param CopyStyle [in]

Flags that control the behavior of the file copy operation. These flags may be a combination of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SP_COPY_DELETESOURCE"></a><a id="sp_copy_deletesource"></a><dl>
<dt><b>SP_COPY_DELETESOURCE</b></dt>
</dl>
</td>
<td width="60%">
Deletes the source file upon successful copy. The caller is not notified if the delete operation fails.

</td>
</tr>
<tr>
<td width="40%"><a id="SP_COPY_REPLACEONLY"></a><a id="sp_copy_replaceonly"></a><dl>
<dt><b>SP_COPY_REPLACEONLY</b></dt>
</dl>
</td>
<td width="60%">
Copies the file only if doing so would overwrite a file at the destination path. If the target does not exist, the function returns <b>FALSE</b> and 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> returns NO_ERROR.

</td>
</tr>
<tr>
<td width="40%"><a id="SP_COPY_NEWER_OR_SAME"></a><a id="sp_copy_newer_or_same"></a><dl>
<dt><b>SP_COPY_NEWER_OR_SAME</b></dt>
</dl>
</td>
<td width="60%">
Examines each file being copied to see if its version resources indicate that it is either the same version or not newer than an existing copy on the target. 




The file version information used during version checks is that specified in the <b>dwFileVersionMS</b> and <b>dwFileVersionLS</b> members of a 
<a href="/windows/desktop/api/verrsrc/ns-verrsrc-vs_fixedfileinfo">VS_FIXEDFILEINFO</a> structure, as filled in by the  version functions. If one of the files does not have version resources, or if they have identical version information, the source file is considered newer.

If the source file is not newer or equal in version, and <i>CopyMsgHandler</i> is specified, the caller is notified and may cancel the copy operation. If <i>CopyMsgHandler</i> is not specified, the file is not copied.

</td>
</tr>
<tr>
<td width="40%"><a id="SP_COPY_NEWER_ONLY"></a><a id="sp_copy_newer_only"></a><dl>
<dt><b>SP_COPY_NEWER_ONLY</b></dt>
</dl>
</td>
<td width="60%">
Examine each file being copied to see if its version resources indicate that it is not newer than an existing copy on the target. If the source file is newer but not equal in version to the existing target, the file is copied.

</td>
</tr>
<tr>
<td width="40%"><a id="SP_COPY_NOOVERWRITE"></a><a id="sp_copy_nooverwrite"></a><dl>
<dt><b>SP_COPY_NOOVERWRITE</b></dt>
</dl>
</td>
<td width="60%">
Check whether the target file exists, and, if so, notify the caller who may veto the copy. If <i>CopyMsgHandler</i> is not specified, the file is not overwritten.

</td>
</tr>
<tr>
<td width="40%"><a id="SP_COPY_NODECOMP"></a><a id="sp_copy_nodecomp"></a><dl>
<dt><b>SP_COPY_NODECOMP</b></dt>
</dl>
</td>
<td width="60%">
Do not decompress the file. When this flag is set, the target file is not given the uncompressed form of the source name (if appropriate). For example, copying F:<i>\x86\cmd.ex_</i> to &#92;&#92;<i>install</i>&#92;<i>temp</i> results in a target file of <i>\\install\temp\cmd.ex_</i>. If the SP_COPY_NODECOMP flag was not specified, the file would be decompressed and the target would be called <i>\\install\temp\cmd.exe</i>. The file name part of <i>DestinationName</i>, if specified, is stripped and replaced with the file name of the source file. When SP_COPY_NODECOMP is specified, no language or version information can be checked.

</td>
</tr>
<tr>
<td width="40%"><a id="SP_COPY_LANGUAGEAWARE"></a><a id="sp_copy_languageaware"></a><dl>
<dt><b>SP_COPY_LANGUAGEAWARE</b></dt>
</dl>
</td>
<td width="60%">
Examine each file being copied to see if its language differs from the language of any existing file already on the target. If so, and <i>CopyMsgHandler</i> is specified, the caller is notified and may cancel the copy. If <i>CopyMsgHandler</i> is not specified, the file is not copied.

</td>
</tr>
<tr>
<td width="40%"><a id="SP_COPY_SOURCE_ABSOLUTE"></a><a id="sp_copy_source_absolute"></a><dl>
<dt><b>SP_COPY_SOURCE_ABSOLUTE</b></dt>
</dl>
</td>
<td width="60%">
<i>SourceFile</i> is a full source path. Do not look it up in the SourceDisksNames section of the INF file.

</td>
</tr>
<tr>
<td width="40%"><a id="SP_COPY_SOURCEPATH_ABSOLUTE"></a><a id="sp_copy_sourcepath_absolute"></a><dl>
<dt><b>SP_COPY_SOURCEPATH_ABSOLUTE</b></dt>
</dl>
</td>
<td width="60%">
<i>SourcePathRoot</i> is the full path part of the source file. Ignore the relative source specified in the SourceDisksNames section of the INF file for the source media where the file is located. This flag is ignored if SP_COPY_SOURCE_ABSOLUTE is specified.

</td>
</tr>
<tr>
<td width="40%"><a id="SP_COPY_FORCE_IN_USE"></a><a id="sp_copy_force_in_use"></a><dl>
<dt><b>SP_COPY_FORCE_IN_USE</b></dt>
</dl>
</td>
<td width="60%">
If the target exists, behaves as if it is in use and queues the file for copying on the next system restart.

</td>
</tr>
<tr>
<td width="40%"><a id="SP_COPY_FORCE_NOOVERWRITE"></a><a id="sp_copy_force_nooverwrite"></a><dl>
<dt><b>SP_COPY_FORCE_NOOVERWRITE</b></dt>
</dl>
</td>
<td width="60%">
Checks whether the target file exists, and, if so, the file is not overwritten. The caller is not notified.

</td>
</tr>
<tr>
<td width="40%"><a id="SP_COPY_FORCE_NEWER"></a><a id="sp_copy_force_newer"></a><dl>
<dt><b>SP_COPY_FORCE_NEWER</b></dt>
</dl>
</td>
<td width="60%">
Examines each file being copied to see if its version resources (or time stamps for non-image files) indicate that it is not newer than an existing copy on the target. If the file being copied is not newer, the file is not copied. The caller is not notified. The function returns <b>FALSE</b>, and 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> returns NO_ERROR.

</td>
</tr>
</table>

### -param CopyMsgHandler [in]

Optional pointer to a callback function to be notified of various conditions that may arise during the file copy operation.

### -param Context [in]

Optional pointer to a caller-defined value that is passed as the first parameter of the callback function.

## -returns

If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

If <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> returns NO_ERROR, the file copy operation was not completed. The file may not have been copied because the file copy operation was unnecessary or because the file callback function returned <b>FALSE</b>.

## -remarks

If a UNC directory is specified as the target directory of a file installation, you must ensure it exists before you call 
<b>SetupInstallFile</b>. The setup functions do not check for the existence of nor create UNC directories. If the target UNC directory does not exist, the file installation will fail.





> [!NOTE]
> The setupapi.h header defines SetupInstallFile as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/SetupApi/functions">Functions</a>



<a href="/windows/desktop/SetupApi/overview">Overview</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupclosefilequeue">SetupCloseFileQueue</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupcommitfilequeuea">SetupCommitFileQueue</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupopenfilequeue">SetupOpenFileQueue</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupqueuecopya">SetupQueueCopy</a>
