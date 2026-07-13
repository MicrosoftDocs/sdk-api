---
UID: NF:setupapi.SetupQueueCopyW
title: SetupQueueCopyW function (setupapi.h)
description: The SetupQueueCopy function adds a single file copy operation to a setup file queue. (Unicode)
helpviewer_keywords: ["SetupQueueCopy", "SetupQueueCopy function [Setup API]", "SetupQueueCopyW", "_setupapi_setupqueuecopy", "setup.setupqueuecopy", "setupapi/SetupQueueCopy", "setupapi/SetupQueueCopyW"]
old-location: setup\setupqueuecopy.htm
tech.root: setup
ms.assetid: c8683438-7a28-4713-8781-45f9bd75b72c
ms.date: 12/05/2018
ms.keywords: SetupQueueCopy, SetupQueueCopy function [Setup API], SetupQueueCopyA, SetupQueueCopyW, _setupapi_setupqueuecopy, setup.setupqueuecopy, setupapi/SetupQueueCopy, setupapi/SetupQueueCopyA, setupapi/SetupQueueCopyW
req.header: setupapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SetupQueueCopyW (Unicode) and SetupQueueCopyA (ANSI)
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
 - SetupQueueCopyW
 - setupapi/SetupQueueCopyW
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
 - SetupQueueCopy
 - SetupQueueCopyA
 - SetupQueueCopyW
---

# SetupQueueCopyW function


## -description

<p class="CCE_Message">[This function is available for use in the operating systems indicated in the Requirements section. It may be altered or unavailable in subsequent versions.   SetupAPI should no longer be used for installing applications. Instead, use the Windows Installer for developing application installers. SetupAPI continues to be used for installing device drivers.]

The 
<b>SetupQueueCopy</b> function adds a single file copy operation to a setup file queue.

## -parameters

### -param QueueHandle [in]

Handle to a setup file queue, as returned by 
<a href="/windows/desktop/api/setupapi/nf-setupapi-setupopenfilequeue">SetupOpenFileQueue</a>.

### -param SourceRootPath [in]

Pointer to a <b>null</b>-terminated string that specifies the root of the source for this copy, such as A:\.

### -param SourcePath [in]

Pointer to a <b>null</b>-terminated string that specifies the path relative to <i>SourceRootPath</i> where the file can be found. This parameter may be <b>NULL</b>.

### -param SourceFilename [in]

Pointer to a <b>null</b>-terminated string that specifies the file name part of the file to be copied.

### -param SourceDescription [in]

Pointer to a <b>null</b>-terminated string that specifies  a description of the source media to be used during disk prompts. This parameter can be <b>NULL</b>.

### -param SourceTagfile [in]

Pointer to a <b>null</b>-terminated string that specifies  a tag file whose presence at <i>SourceRootPath</i> indicates the presence of the source media. This parameter may be <b>NULL</b>. If not specified, the file itself will be used as the tag file if required.

### -param TargetDirectory [in]

Pointer to a <b>null</b>-terminated string that specifies the directory where the file is to be copied.

### -param TargetFilename [in]

Pointer to a <b>null</b>-terminated string that specifies  the name of the target file. This parameter may be <b>NULL</b>. If not specified, the target file will have the same name as the source file.

### -param CopyStyle [in]

Specifies the behavior of the file copy operation. This parameter may be a combination of the following values. 







#### SP_COPY_DELETESOURCE

Delete the source file upon successful copy. The caller is not notified if the delete fails.



#### SP_COPY_REPLACEONLY

Copy the file only if doing so would overwrite a file at the destination path. The caller is not notified.



#### SP_COPY_NEWER_OR SAME

Examine each file being copied to see if its version resources indicate that it is either the same version or not newer than an existing copy on the target. 




The file version information used during version checks is that specified in the <b>dwFileVersionMS</b> and <b>dwFileVersionLS</b> members of a 
<a href="/windows/desktop/api/verrsrc/ns-verrsrc-vs_fixedfileinfo">VS_FIXEDFILEINFO</a> structure, as filled in by the  version functions. If one of the files does not have version resources, or if they have identical version information, the source file is considered newer.

If the source file is not equal in version or newer, and <i>CopyMsgHandler</i> is specified, the caller is notified and may cancel the copy. If <i>CopyMsgHandler</i> is not specified, the file is not copied.



#### SP_COPY_NEWER_ONLY

Examine each file being copied to see if its version resources indicate that it is not newer than an existing copy on the target. If the source file is newer but not equal in version to the existing target, the file is copied.



#### SP_COPY_NOOVERWRITE

Check whether the target file exists, and, if so, notify the caller who may veto the copy. If <i>CopyMsgHandler</i> is not specified, the file is not overwritten.



#### SP_COPY_NODECOMP

Do not decompress the file. When this flag is set, the target file is not given the uncompressed form of the source name (if appropriate). For example, copying f:\x86\cmd.ex_ to \\install\temp results in a target file of \\install\temp\cmd.ex_. If the SP_COPY_NODECOMP flag was not specified, the file would be decompressed and the target would be called \\install\temp\cmd.exe. The filename part of <i>DestinationName</i>, if specified, is stripped and replaced with the filename of the source file. When SP_COPY_NODECOMP is specified, no language or version information can be checked.



#### SP_COPY_LANGUAGEAWARE

Examine each file being copied to see if its language differs from the language of any existing file already on the target. If so, and <i>CopyMsgHandler</i> is specified, the caller is notified and may cancel the copy. If <i>CopyMsgHandler</i> is not specified, the file is not copied.



#### SP_COPY_SOURCE_ABSOLUTE

<i>SourceFile</i> is a full source path. Do not look it up in the <b>SourceDisksNames</b> section of the INF file.



#### SP_COPY_SOURCEPATH_ABSOLUTE

<i>SourcePathRoot</i> is the full path part of the source file. Ignore the relative source specified in the <b>SourceDisksNames</b> section of the INF file for the source media where the file is located. This flag is ignored if SP_COPY_SOURCE_ABSOLUTE is specified.



#### SP_COPY_FORCE_IN_USE

If the target exists, behave as if it is in use and queue the file for copying on the next system reboot.



#### SP_COPY_IN_USE_NEEDS_REBOOT

If the file was in use during the copy operation, alert the user that the system needs to be rebooted.



#### SP_COPY_NOSKIP

Do not give the user the option to skip a file.



#### SP_COPY_FORCE_NOOVERWRITE

Check whether the target file exists, and, if so, the file is not overwritten. The caller is not notified.



#### SP_COPY_FORCE_NEWER

Examine each file being copied to see if its version resources (or time stamps for non-image files) indicate that it is not newer than an existing copy on the target. If the file being copied is not newer, the file is not copied. The caller is not notified.



#### SP_COPY_WARNIFSKIP

If the user tries to skip a file, warn them that skipping a file may affect the installation. (Used for system-critical files.)


##### - CopyStyle.SP_COPY_DELETESOURCE

Delete the source file upon successful copy. The caller is not notified if the delete fails.


##### - CopyStyle.SP_COPY_FORCE_IN_USE

If the target exists, behave as if it is in use and queue the file for copying on the next system reboot.


##### - CopyStyle.SP_COPY_FORCE_NEWER

Examine each file being copied to see if its version resources (or time stamps for non-image files) indicate that it is not newer than an existing copy on the target. If the file being copied is not newer, the file is not copied. The caller is not notified.


##### - CopyStyle.SP_COPY_FORCE_NOOVERWRITE

Check whether the target file exists, and, if so, the file is not overwritten. The caller is not notified.


##### - CopyStyle.SP_COPY_IN_USE_NEEDS_REBOOT

If the file was in use during the copy operation, alert the user that the system needs to be rebooted.


##### - CopyStyle.SP_COPY_LANGUAGEAWARE

Examine each file being copied to see if its language differs from the language of any existing file already on the target. If so, and <i>CopyMsgHandler</i> is specified, the caller is notified and may cancel the copy. If <i>CopyMsgHandler</i> is not specified, the file is not copied.


##### - CopyStyle.SP_COPY_NEWER_ONLY

Examine each file being copied to see if its version resources indicate that it is not newer than an existing copy on the target. If the source file is newer but not equal in version to the existing target, the file is copied.


##### - CopyStyle.SP_COPY_NEWER_OR SAME

Examine each file being copied to see if its version resources indicate that it is either the same version or not newer than an existing copy on the target. 




The file version information used during version checks is that specified in the <b>dwFileVersionMS</b> and <b>dwFileVersionLS</b> members of a 
<a href="/windows/desktop/api/verrsrc/ns-verrsrc-vs_fixedfileinfo">VS_FIXEDFILEINFO</a> structure, as filled in by the  version functions. If one of the files does not have version resources, or if they have identical version information, the source file is considered newer.

If the source file is not equal in version or newer, and <i>CopyMsgHandler</i> is specified, the caller is notified and may cancel the copy. If <i>CopyMsgHandler</i> is not specified, the file is not copied.


##### - CopyStyle.SP_COPY_NODECOMP

Do not decompress the file. When this flag is set, the target file is not given the uncompressed form of the source name (if appropriate). For example, copying f:\x86\cmd.ex_ to \\install\temp results in a target file of \\install\temp\cmd.ex_. If the SP_COPY_NODECOMP flag was not specified, the file would be decompressed and the target would be called \\install\temp\cmd.exe. The filename part of <i>DestinationName</i>, if specified, is stripped and replaced with the filename of the source file. When SP_COPY_NODECOMP is specified, no language or version information can be checked.


##### - CopyStyle.SP_COPY_NOOVERWRITE

Check whether the target file exists, and, if so, notify the caller who may veto the copy. If <i>CopyMsgHandler</i> is not specified, the file is not overwritten.


##### - CopyStyle.SP_COPY_NOSKIP

Do not give the user the option to skip a file.


##### - CopyStyle.SP_COPY_REPLACEONLY

Copy the file only if doing so would overwrite a file at the destination path. The caller is not notified.


##### - CopyStyle.SP_COPY_SOURCEPATH_ABSOLUTE

<i>SourcePathRoot</i> is the full path part of the source file. Ignore the relative source specified in the <b>SourceDisksNames</b> section of the INF file for the source media where the file is located. This flag is ignored if SP_COPY_SOURCE_ABSOLUTE is specified.


##### - CopyStyle.SP_COPY_SOURCE_ABSOLUTE

<i>SourceFile</i> is a full source path. Do not look it up in the <b>SourceDisksNames</b> section of the INF file.


##### - CopyStyle.SP_COPY_WARNIFSKIP

If the user tries to skip a file, warn them that skipping a file may affect the installation. (Used for system-critical files.)

## -returns

If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

If a UNC directory is specified as the target directory of a file copy operation, you must ensure it exists before the queue is committed. The setup functions do not check for the existence of and do not create UNC directories. If the target UNC directory does not exist, the file copy will fail.





> [!NOTE]
> The setupapi.h header defines SetupQueueCopy as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/SetupApi/functions">Functions</a>



<a href="/windows/desktop/SetupApi/overview">Overview</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupqueuecopysectiona">SetupQueueCopySection</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupqueuedefaultcopya">SetupQueueDefaultCopy</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupqueuedeletea">SetupQueueDelete</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupqueuerenamea">SetupQueueRename</a>
