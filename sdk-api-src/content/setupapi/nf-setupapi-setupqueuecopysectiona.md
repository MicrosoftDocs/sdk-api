---
UID: NF:setupapi.SetupQueueCopySectionA
title: SetupQueueCopySectionA function
author: windows-sdk-content
description: The SetupQueueCopySection function places all the files in a section of an INF file in a setup queue for copying.
old-location: setup\setupqueuecopysection.htm
old-project: SetupApi
ms.assetid: f61fd00e-e60f-4722-9da7-1ed4d8491004
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: SetupQueueCopySection, SetupQueueCopySection function [Setup API], SetupQueueCopySectionA, SetupQueueCopySectionW, _setupapi_setupqueuecopysection, setup.setupqueuecopysection, setupapi/SetupQueueCopySection, setupapi/SetupQueueCopySectionA, setupapi/SetupQueueCopySectionW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: setupapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SetupQueueCopySectionW (Unicode) and SetupQueueCopySectionA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: TSSD_ConnectionPoint, *PTSSD_ConnectionPoint
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Setupapi.dll
api_name:
-	SetupQueueCopySection
-	SetupQueueCopySectionA
-	SetupQueueCopySectionW
product: Windows
targetos: Windows
req.lib: Setupapi.lib
req.dll: Setupapi.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# SetupQueueCopySectionA function


## -description


<p class="CCE_Message">[This function is available for use in the operating systems indicated in the Requirements section. It may be altered or unavailable in subsequent versions.   SetupAPI should no longer be used for installing applications. Instead, use the Windows Installer for developing application installers. SetupAPI continues to be used for installing device drivers.]

The 
<b>SetupQueueCopySection</b> function places all the files in a section of an INF file in a setup queue for copying. The section must be in the correct <b>Copy Files</b> format and the INF file must contain <b>SourceDisksFiles</b> and <b>SourceDisksNames</b> sections (or have had the INF files containing those sections appended).


## -parameters




### -param QueueHandle [in]

Handle to a setup file queue, as returned by 
<a href="https://msdn.microsoft.com/36950f18-80ae-46b7-9f9f-bd5307d72a3b">SetupOpenFileQueue</a>.


### -param SourceRootPath [in]

Pointer to a null-terminated string that specifies the root of the source for this copy, such as A:\.


### -param InfHandle [in]

Handle to an open INF file that contains the <b>SourceDisksFiles</b> and <b>SourceDisksNames</b> sections. If <i>ListInfHandle</i> is not specified, <i>InfHandle</i> contains the section names. If platform-specific sections exist for the user's system (for example, SourceDisksNames.x86 and SourceDisksFiles.x86), the platform-specific section will be used.


### -param ListInfHandle [in]

Optional handle to an open INF file that contains the section to queue for copying. If <i>ListInfHandle</i> is not specified, <i>InfHandle</i> is assumed to contain the section.


### -param Section [in]

Pointer to a null-terminated string that specifies the name of the section to be queued for copy.


### -param CopyStyle [in]

Flags that control the behavior of the file copy operation. These flags may be a combination of the following values. 







#### SP_COPY_DELETESOURCE

Delete the source file upon successful copy. The caller is not notified if the delete fails.



#### SP_COPY_REPLACEONLY

Copy the file only if doing so would overwrite a file at the destination path.



#### SP_COPY_NEWER_OR_SAME

Examine each file being copied to see if its version resources indicate that it is either equal in version or not newer than an existing copy on the target. 




The file version information used during version checks is that specified in the <b>dwFileVersionMS</b> and <b>dwFileVersionLS</b> members of a 
<a href="_win32_vs_fixedfileinfo_str_cpp">VS_FIXEDFILEINFO</a> structure, as filled in by the  version functions. If one of the files does not have version resources, or if they have identical version information, the source file is considered newer.

If the source file is not equal in version or newer, and <i>CopyMsgHandler</i> is specified, the caller is notified and may cancel the copy. If <i>CopyMsgHandler</i> is not specified, the file is not copied.



#### SP_COPY_NEWER_ONLY

Examine each file being copied to see if its version resources indicate that it is not newer than an existing copy on the target. If the source file is newer but not equal in version to the existing target, the file is copied.



#### SP_COPY_NOOVERWRITE

Check whether the target file exists, and, if so, notify the caller who may veto the copy. If <i>CopyMsgHandler</i> is not specified, the file is not overwritten.



#### SP_COPY_NODECOMP

Do not decompress the file. When this flag is set, the target file is not given the uncompressed form of the source name (if appropriate). For example, copying f:\x86s\cmd.ex_ to \\install\temp results in a target file of \\install\temp\cmd.ex_. If the SP_COPY_NODECOMP flag was not specified, the file would be decompressed and the target would be called \\install\temp\cmd.exe. The filename part of <i>DestinationName</i>, if specified, is stripped and replaced with the filename of the source file. When SP_COPY_NODECOMP is specified, no language or version information can be checked.



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


## -returns



If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



If a UNC directory is specified as the target directory of a file copy operation, you must ensure it exists before the queue is committed. The setup functions do not check for the existence of and do not create UNC directories. If the target UNC directory does not exist, the file copy will fail.

This function requires a Windows INF file. Some older INF file  formats may not be supported. 




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn938561">Functions</a>



<a href="https://msdn.microsoft.com/58201596-cb8c-480a-abef-896c1f9ef098">Overview</a>



<a href="https://msdn.microsoft.com/c8683438-7a28-4713-8781-45f9bd75b72c">SetupQueueCopy</a>



<a href="https://msdn.microsoft.com/57e8dc72-5b0e-486c-9819-fa44085580eb">SetupQueueDefaultCopy</a>
 

 

