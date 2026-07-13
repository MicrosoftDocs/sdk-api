---
UID: NS:setupapi._SP_FILE_COPY_PARAMS_A
title: SP_FILE_COPY_PARAMS_A (setupapi.h)
description: The SP_FILE_COPY_PARAMS structure describes a single file copy operation. (ANSI)
helpviewer_keywords: ["*PSP_FILE_COPY_PARAMS_A","PSP_FILE_COPY_PARAMS","PSP_FILE_COPY_PARAMS structure pointer [Setup API]","SP_COPY_DELETESOURCE","SP_COPY_FORCE_IN_USE","SP_COPY_FORCE_NEWER","SP_COPY_FORCE_NOOVERWRITE","SP_COPY_IN_USE_NEEDS_REBOOT","SP_COPY_LANGUAGEAWARE","SP_COPY_NEWER_ONLY","SP_COPY_NEWER_OR_SAME","SP_COPY_NODECOMP","SP_COPY_NOOVERWRITE","SP_COPY_NOSKIP","SP_COPY_REPLACEONLY","SP_COPY_SOURCEPATH_ABSOLUTE","SP_COPY_SOURCE_ABSOLUTE","SP_COPY_WARNIFSKIP","SP_FILE_COPY_PARAMS","SP_FILE_COPY_PARAMS structure [Setup API]","SP_FILE_COPY_PARAMS_A","_setupapi_sp_file_copy_params","setup.sp_file_copy_params","setupapi/PSP_FILE_COPY_PARAMS","setupapi/SP_FILE_COPY_PARAMS"]
old-location: setup\sp_file_copy_params.htm
tech.root: setup
ms.assetid: 4c4d418d-e279-40ea-9ec1-42ced523db34
ms.date: 12/05/2018
ms.keywords: '*PSP_FILE_COPY_PARAMS_A, PSP_FILE_COPY_PARAMS, PSP_FILE_COPY_PARAMS structure pointer [Setup API], SP_COPY_DELETESOURCE, SP_COPY_FORCE_IN_USE, SP_COPY_FORCE_NEWER, SP_COPY_FORCE_NOOVERWRITE, SP_COPY_IN_USE_NEEDS_REBOOT, SP_COPY_LANGUAGEAWARE, SP_COPY_NEWER_ONLY, SP_COPY_NEWER_OR_SAME, SP_COPY_NODECOMP, SP_COPY_NOOVERWRITE, SP_COPY_NOSKIP, SP_COPY_REPLACEONLY, SP_COPY_SOURCEPATH_ABSOLUTE, SP_COPY_SOURCE_ABSOLUTE, SP_COPY_WARNIFSKIP, SP_FILE_COPY_PARAMS, SP_FILE_COPY_PARAMS structure [Setup API], SP_FILE_COPY_PARAMS_A, _setupapi_sp_file_copy_params, setup.sp_file_copy_params, setupapi/PSP_FILE_COPY_PARAMS, setupapi/SP_FILE_COPY_PARAMS'
req.header: setupapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: SP_FILE_COPY_PARAMS_A, *PSP_FILE_COPY_PARAMS_A
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SP_FILE_COPY_PARAMS_A
 - setupapi/_SP_FILE_COPY_PARAMS_A
 - PSP_FILE_COPY_PARAMS_A
 - setupapi/PSP_FILE_COPY_PARAMS_A
 - SP_FILE_COPY_PARAMS_A
 - setupapi/SP_FILE_COPY_PARAMS_A
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Setupapi.h
api_name:
 - SP_FILE_COPY_PARAMS
 - sp_file_copy_params_a
---

# SP_FILE_COPY_PARAMS_A structure


## -description

The 
<b>SP_FILE_COPY_PARAMS</b> structure describes a single file copy operation.

## -struct-fields

### -field cbSize

Size of the structure, in bytes. Set to the value: <code>sizeof(SP_FILE_COPY_PARAMS)</code>.

### -field QueueHandle

Handle to a setup file queue, as returned by 
<a href="/windows/desktop/api/setupapi/nf-setupapi-setupopenfilequeue">SetupOpenFileQueue</a>.

### -field SourceRootPath

Optional pointer to the root of the source for this copy, such as A:\.

### -field SourcePath

Optional pointer to the path relative to <b>SourceRootPath</b> where the file can be found.

### -field SourceFilename

File name part of the file to be copied.

### -field SourceDescription

Optional pointer to a description of the source media to be used during disk prompts.

### -field SourceTagfile

Optional pointer to a tag file whose presence at <b>SourceRootPath</b> indicates the presence of the source media. If not specified, the file itself will be used as the tag file if required.

### -field TargetDirectory

Directory where the file is to be copied.

### -field TargetFilename

Optional pointer to the name of the target file. If not specified, the target file will have the same name as the source file.

### -field CopyStyle

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
Delete the source file upon successful copy. The caller is not notified if the deletion fails.

</td>
</tr>
<tr>
<td width="40%"><a id="SP_COPY_REPLACEONLY"></a><a id="sp_copy_replaceonly"></a><dl>
<dt><b>SP_COPY_REPLACEONLY</b></dt>
</dl>
</td>
<td width="60%">
Copy the file only if doing so would overwrite a file at the destination path. The caller is not notified.

</td>
</tr>
<tr>
<td width="40%"><a id="SP_COPY_NEWER_OR_SAME"></a><a id="sp_copy_newer_or_same"></a><dl>
<dt><b>SP_COPY_NEWER_OR_SAME</b></dt>
</dl>
</td>
<td width="60%">
Examine each file being copied to see if its version resources indicate that it is either the same version or not newer than an existing copy on the target. 


The file version information used during version checks is that specified in the <b>dwFileVersionMS</b> and <b>dwFileVersionLS</b> members of a 
<a href="/windows/desktop/api/verrsrc/ns-verrsrc-vs_fixedfileinfo">VS_FIXEDFILEINFO</a> structure, as filled in by the version functions. If one of the files does not have version resources, or if they have identical version information, the source file is considered newer.

If the source file is not equal in version or newer, and <i>CopyMsgHandler</i> is specified, the caller is notified and may cancel the copy. If <i>CopyMsgHandler</i> is not specified, the file is not copied.

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
Check whether the target file exists, and if so, notify the caller who may veto the copy. If <i>CopyMsgHandler</i> is not specified, the file is not overwritten.

</td>
</tr>
<tr>
<td width="40%"><a id="SP_COPY_NODECOMP"></a><a id="sp_copy_nodecomp"></a><dl>
<dt><b>SP_COPY_NODECOMP</b></dt>
</dl>
</td>
<td width="60%">
Do not decompress the file. When this flag is set, the target file is not given the uncompressed form of the source name (if appropriate). For example, copying f:\x86\cmd.ex_ to \\install\temp results in a target file of \\install\temp\cmd.ex_. If the SP_COPY_NODECOMP flag was not specified, the file would be decompressed and the target would be called \\install\temp\cmd.exe. The file name part of <i>DestinationName</i>, if specified, is stripped and replaced with the file name of the source file. When SP_COPY_NODECOMP is specified, no language or version information can be checked.

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
If the target exists, behave as if it is in-use and queue the file for copying on the next system reboot.

</td>
</tr>
<tr>
<td width="40%"><a id="SP_COPY_IN_USE_NEEDS_REBOOT"></a><a id="sp_copy_in_use_needs_reboot"></a><dl>
<dt><b>SP_COPY_IN_USE_NEEDS_REBOOT</b></dt>
</dl>
</td>
<td width="60%">
If the file was in-use during the copy operation, alert the user that the system needs to be rebooted.

</td>
</tr>
<tr>
<td width="40%"><a id="SP_COPY_NOSKIP"></a><a id="sp_copy_noskip"></a><dl>
<dt><b>SP_COPY_NOSKIP</b></dt>
</dl>
</td>
<td width="60%">
Do not give the user the option to skip a file.

</td>
</tr>
<tr>
<td width="40%"><a id="SP_COPY_FORCE_NOOVERWRITE"></a><a id="sp_copy_force_nooverwrite"></a><dl>
<dt><b>SP_COPY_FORCE_NOOVERWRITE</b></dt>
</dl>
</td>
<td width="60%">
Check whether the target file exists, and if so, the file is not overwritten. The caller is not notified.

</td>
</tr>
<tr>
<td width="40%"><a id="SP_COPY_FORCE_NEWER"></a><a id="sp_copy_force_newer"></a><dl>
<dt><b>SP_COPY_FORCE_NEWER</b></dt>
</dl>
</td>
<td width="60%">
Examine each file being copied to see if its version resources (or time stamps for non-image files) indicate that it is not newer than an existing copy on the target. If the file being copied is not newer, the file is not copied. The caller is not notified.

</td>
</tr>
<tr>
<td width="40%"><a id="SP_COPY_WARNIFSKIP"></a><a id="sp_copy_warnifskip"></a><dl>
<dt><b>SP_COPY_WARNIFSKIP</b></dt>
</dl>
</td>
<td width="60%">
If the user tries to skip a file, warn them that skipping a file may affect the installation. (Used for system-critical files.)

</td>
</tr>
</table>

### -field LayoutInf

Handle to the INF to use to obtain source information.

### -field SecurityDescriptor

An optional Security Descriptor String specifying the ACL to apply to the file.

## -see-also

<a href="/windows/desktop/SetupApi/overview">Overview</a>



<a href="/windows/desktop/SetupApi/structures--setup-api-">Structures</a>

## -remarks

> [!NOTE]
> The setupapi.h header defines SP_FILE_COPY_PARAMS as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
