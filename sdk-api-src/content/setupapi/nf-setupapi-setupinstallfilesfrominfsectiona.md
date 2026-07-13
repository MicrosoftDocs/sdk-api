---
UID: NF:setupapi.SetupInstallFilesFromInfSectionA
title: SetupInstallFilesFromInfSectionA function (setupapi.h)
description: The SetupInstallFilesFromInfSection function queues all the files for an installation that are specified in the Copy Files, Delete Files, and Rename Files sections that are listed by an Install section. (ANSI)
helpviewer_keywords: ["SetupInstallFilesFromInfSectionA", "setupapi/SetupInstallFilesFromInfSectionA"]
old-location: setup\setupinstallfilesfrominfsection.htm
tech.root: setup
ms.assetid: 9834a3b0-f8f5-4e4d-92b2-d3c5a4939a41
ms.date: 12/20/2024
ms.keywords: SetupInstallFilesFromInfSection, SetupInstallFilesFromInfSection function [Setup API], SetupInstallFilesFromInfSectionA, SetupInstallFilesFromInfSectionW, _setupapi_setupinstallfilesfrominfsection, setup.setupinstallfilesfrominfsection, setupapi/SetupInstallFilesFromInfSection, setupapi/SetupInstallFilesFromInfSectionA, setupapi/SetupInstallFilesFromInfSectionW
req.header: setupapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SetupInstallFilesFromInfSectionW (Unicode) and SetupInstallFilesFromInfSectionA (ANSI)
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
 - SetupInstallFilesFromInfSectionA
 - setupapi/SetupInstallFilesFromInfSectionA
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
 - SetupInstallFilesFromInfSection
 - SetupInstallFilesFromInfSectionA
 - SetupInstallFilesFromInfSectionW
---

# SetupInstallFilesFromInfSectionA function


## -description

<p class="CCE_Message">[This function is available for use in the operating systems indicated in the Requirements section. It may be altered or unavailable in subsequent versions.   SetupAPI should no longer be used for installing applications. Instead, use the Windows Installer for developing application installers. SetupAPI continues to be used for installing device drivers.]

The 
<b>SetupInstallFilesFromInfSection</b> function queues all the files for an installation that are specified in the Copy Files, Delete Files, and Rename Files sections that are listed by an Install section.

If a file is modified, the caller of this function is required to have privileges to write to the target directory.

## -parameters

### -param InfHandle [in]

The handle to an INF file that contains the section to be installed.

### -param LayoutInfHandle [in]

An optional pointer to a handle to the INF file that contains the SourceDisksFiles and SourceDisksNames sections. 

If <i>LayoutInfHandle</i> is not specified, then the SourceDisksFiles and SourceDisksNames sections from <i>InfHandle</i> are used.

### -param FileQueue [in]

The handle to the queue where installation operations are to be added.

### -param SectionName [in]

The name of the Install section in  the <i>InfHandle</i> parameter that lists the Copy Files, Delete Files, and  Rename Files sections that contain the files to install. 

Use a <b>null</b>-terminated string.

### -param SourceRootPath [in]

An optional pointer to a root path to the source files to copy, for example, A:\ or \\pegasus\win\install. 

Use a <b>null</b>-terminated string.

### -param CopyFlags [in]

An optional pointer to a set of flags that control the behavior of the file copy operation. 

The flags can be a combination of the following values. 







#### SP_COPY_DELETESOURCE

Deletes the source file when the copy task succeeds. 

The caller is not notified if a delete task fails.



#### SP_COPY_REPLACEONLY

Copies a file only to overwrite a file at the destination path.



#### SP_COPY_NEWER_OR_SAME

Examines each file that is copied to determine whether the version resources indicate that it is the same version, or not newer than an existing copy on the target. 

If the source file is not a newer or equal version, the function notifies the caller who can cancel the copy.   




The file version information that is used during version checks is specified in the <b>dwFileVersionMS </b> and <b>dwFileVersionLS</b> members of a 
<a href="/windows/desktop/api/verrsrc/ns-verrsrc-vs_fixedfileinfo">VS_FIXEDFILEINFO</a> structure, as filled in by the Win32 version functions.

 If one of the files does not have version resources, or if they have identical version information, the source file is considered newer.



#### SP_COPY_NEWER_ONLY

Examines each file that is being copied to determine whether its version resources indicate that it is not newer than an existing copy on the target. 

If the source file is newer but not equal in version to the existing target, the file is copied.



#### SP_COPY_NOOVERWRITE

Checks to determine whether or not the target file exists.  

If the target file exists, the function notifies the caller who can cancel the copy.



#### SP_COPY_NODECOMP

Does not decompress a file. 

When this flag is set, the target file is not given the uncompressed form of the source name, for example, if you copy f:\x86\cmd.ex_ to \\install\temp the result is the following target file: \\install\temp\cmd.ex_.

 If the SP_COPY_NODECOMP flag is not specified, the file is decompressed and the target is called \\install\temp\cmd.exe. 

The filename part of DestinationName, if specified, is deleted and replaced with the filename of the source file. When SP_COPY_NODECOMP is specified, language and version information cannot be checked.



#### SP_COPY_LANGUAGEAWARE

Examines each file that is being copied to determine whether or not the language is different from the language of any existing file already on the target. 

If the language  is different, the function notifies the caller who can cancel the copy task. 



#### SP_COPY_SOURCE_ABSOLUTE

SourceFile is a full source path. 

Do not look it up in the SourceDisksNames section of the INF file.



#### SP_COPY_SOURCEPATH_ABSOLUTE

SourcePathRoot is the full path part of the source file. 

Ignore the relative source that is specified in the SourceDisksNames section of the INF file for the source media where the file is located. This flag is ignored if SP_COPY_SOURCE_ABSOLUTE is specified.



#### SP_COPY_FORCE_IN_USE

Queues the file for copying on the next system reboot, if the target exists and is being used.



#### SP_COPY_IN_USE_NEEDS_REBOOT

Alerts the user that the system needs to be rebooted, if the file is being used during a copy operation.



#### SP_COPY_NOSKIP

Does not give the user the option to skip a file.



#### SP_COPY_FORCE_NOOVERWRITE

Checks to determine whether or not the target file exists, and if the target exists, the file is not overwritten and the caller is not notified.



#### SP_COPY_FORCE_NEWER

Examines each file that is being copied to identify that its version resources (or time stamps for non-image files) indicate that it is not newer than an existing copy on the target. 

If the file that is being copied is not newer, the file is not copied, and the caller is not notified.



#### SP_COPY_WARNIFSKIP

Warns that skipping a file may affect an installation if the user tries to skip a file. 

Use this flag  for system-critical files.

## -returns

If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is 0 (zero). To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

<b>SetupInstallFilesFromInfSection</b> can be called multiple times to queue the files that are specified in multiple INF sections. After the queue is committed successfully and the files are copied, renamed, and/or deleted, 
<a href="/windows/desktop/api/setupapi/nf-setupapi-setupinstallfrominfsectiona">SetupInstallFromInfSection</a> can be called to perform registry and INI installation operations.

If a UNC directory is specified as the target directory of a file installation, you must ensure that the UNC directory exists before you call 
<b>SetupInstallFilesFromInfSection</b>. The setup functions do not check for the existence of directories and do not create UNC directories. If the target UNC directory does not exist, the file installation fails.

> [!NOTE]
> The setupapi.h header defines SetupInstallFilesFromInfSection as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

<b>SetupInstallFilesFromInfSection</b> will log diagnostic information to the [SetupAPI application installation text log](/windows-hardware/drivers/install/setupapi-text-logs). This log file is generally off by default. It can be enabled by modifying the *General logging levels* part of the SetupAPI `LogLevel` value as described at [Setting SetupAPI Logging Levels](/windows-hardware/drivers/install/setting-setupapi-logging-levels). For performance reasons, you should only enable this log file when troubleshooting an issue. When the log file is enabled, you can find it at `%windir%\inf\setupapi.app.log`.

## -see-also

<a href="/windows/desktop/SetupApi/functions">Functions</a>



<a href="/windows/desktop/SetupApi/overview">Overview</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupinstallfrominfsectiona">SetupInstallFromInfSection</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupinstallservicesfrominfsectiona">SetupInstallServicesFromInfSection</a>
