---
UID: NF:setupapi.SetupQueueDefaultCopyW
title: SetupQueueDefaultCopyW function (setupapi.h)
description: The SetupQueueDefaultCopy function adds a single file to a setup file queue for copying, using the default source media and destination as specified in an INF file. (Unicode)
helpviewer_keywords: ["SetupQueueDefaultCopy", "SetupQueueDefaultCopy function [Setup API]", "SetupQueueDefaultCopyW", "_setupapi_setupqueuedefaultcopy", "setup.setupqueuedefaultcopy", "setupapi/SetupQueueDefaultCopy", "setupapi/SetupQueueDefaultCopyW"]
old-location: setup\setupqueuedefaultcopy.htm
tech.root: setup
ms.assetid: 57e8dc72-5b0e-486c-9819-fa44085580eb
ms.date: 12/05/2018
ms.keywords: SetupQueueDefaultCopy, SetupQueueDefaultCopy function [Setup API], SetupQueueDefaultCopyA, SetupQueueDefaultCopyW, _setupapi_setupqueuedefaultcopy, setup.setupqueuedefaultcopy, setupapi/SetupQueueDefaultCopy, setupapi/SetupQueueDefaultCopyA, setupapi/SetupQueueDefaultCopyW
req.header: setupapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SetupQueueDefaultCopyW (Unicode) and SetupQueueDefaultCopyA (ANSI)
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
 - SetupQueueDefaultCopyW
 - setupapi/SetupQueueDefaultCopyW
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
 - SetupQueueDefaultCopy
 - SetupQueueDefaultCopyA
 - SetupQueueDefaultCopyW
---

# SetupQueueDefaultCopyW function


## -description

<p class="CCE_Message">[This function is available for use in the operating systems indicated in the Requirements section. It may be altered or unavailable in subsequent versions.   SetupAPI should no longer be used for installing applications. Instead, use the Windows Installer for developing application installers. SetupAPI continues to be used for installing device drivers.]

The 
<b>SetupQueueDefaultCopy</b> function adds a single file to a setup file queue for copying, using the default source media and destination as specified in an INF file.

## -parameters

### -param QueueHandle [in]

Handle to a setup file queue, as returned by 
<a href="/windows/desktop/api/setupapi/nf-setupapi-setupopenfilequeue">SetupOpenFileQueue</a>.

### -param InfHandle [in]

Handle to an open INF file that contains the <b>SourceDisksFiles</b> and <b>SourceDisksNames</b> sections. If platform-specific sections exist for the user's system (for example, <b>SourceDisksNames.x86</b> and <b>SourceDisksFiles.x86</b>), the platform-specific section will be used.

### -param SourceRootPath [in]

Pointer to a null-terminated string that specifies the root directory of the source for this copy such as A:\.

### -param SourceFilename [in]

Pointer to a null-terminated string that specifies the file name of the file to be copied.

### -param TargetFilename [in]

Pointer to a null-terminated string that specifies the file name of the target file.

### -param CopyStyle [in]

Flags that control the behavior of the file copy operation. These flags may be a combination of the following values. 







#### SP_COPY_DELETESOURCE

Delete the source file upon successful copy. The caller is not notified if the delete fails.



#### SP_COPY_REPLACEONLY

Copy the file only if doing so would overwrite a file at the destination path.



#### SP_COPY_NEWER_OR_SAME

Examine each file being copied to see if its version resources indicate that it is either equal in version or not newer than an existing copy on the target. 




The file version information used during version checks is that specified in the <b>dwFileVersionMS</b> and <b>dwFileVersionLS</b> members of a 
<a href="/windows/desktop/api/verrsrc/ns-verrsrc-vs_fixedfileinfo">VS_FIXEDFILEINFO</a> structure, as filled in by the version functions. If one of the files does not have version resources, or if they have identical version information, the source file is considered newer.

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


##### - CopyStyle.SP_COPY_NEWER_OR_SAME

Examine each file being copied to see if its version resources indicate that it is either equal in version or not newer than an existing copy on the target. 




The file version information used during version checks is that specified in the <b>dwFileVersionMS</b> and <b>dwFileVersionLS</b> members of a 
<a href="/windows/desktop/api/verrsrc/ns-verrsrc-vs_fixedfileinfo">VS_FIXEDFILEINFO</a> structure, as filled in by the version functions. If one of the files does not have version resources, or if they have identical version information, the source file is considered newer.

If the source file is not equal in version or newer, and <i>CopyMsgHandler</i> is specified, the caller is notified and may cancel the copy. If <i>CopyMsgHandler</i> is not specified, the file is not copied.


##### - CopyStyle.SP_COPY_NODECOMP

Do not decompress the file. When this flag is set, the target file is not given the uncompressed form of the source name (if appropriate). For example, copying f:\x86\cmd.ex_ to \\install\temp results in a target file of \\install\temp\cmd.ex_. If the SP_COPY_NODECOMP flag was not specified, the file would be decompressed and the target would be called \\install\temp\cmd.exe. The filename part of <i>DestinationName</i>, if specified, is stripped and replaced with the filename of the source file. When SP_COPY_NODECOMP is specified, no language or version information can be checked.


##### - CopyStyle.SP_COPY_NOOVERWRITE

Check whether the target file exists, and, if so, notify the caller who may veto the copy. If <i>CopyMsgHandler</i> is not specified, the file is not overwritten.


##### - CopyStyle.SP_COPY_NOSKIP

Do not give the user the option to skip a file.


##### - CopyStyle.SP_COPY_REPLACEONLY

Copy the file only if doing so would overwrite a file at the destination path.


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

The default destination used by this function is specified by the <b>DefaultDestDir</b> key in the <b>DestinationDirs</b> section of an INF file.

This function requires a Windows INF file. Some older INF file  formats may not be supported. 





> [!NOTE]
> The setupapi.h header defines SetupQueueDefaultCopy as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/SetupApi/functions">Functions</a>



<a href="/windows/desktop/SetupApi/overview">Overview</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupqueuecopya">SetupQueueCopy</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupqueuecopysectiona">SetupQueueCopySection</a>
