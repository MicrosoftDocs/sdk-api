---
UID: NF:setupapi.SetupQueueCopyA
title: SetupQueueCopyA function
author: windows-sdk-content
description: The SetupQueueCopy function adds a single file copy operation to a setup file queue.
old-location: setup\setupqueuecopy.htm
old-project: SetupApi
ms.assetid: c8683438-7a28-4713-8781-45f9bd75b72c
ms.author: windowssdkdev
ms.date: 08/03/2018
ms.keywords: SetupQueueCopy, SetupQueueCopy function [Setup API], SetupQueueCopyA, SetupQueueCopyW, _setupapi_setupqueuecopy, setup.setupqueuecopy, setupapi/SetupQueueCopy, setupapi/SetupQueueCopyA, setupapi/SetupQueueCopyW
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
req.unicode-ansi: SetupQueueCopyW (Unicode) and SetupQueueCopyA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: TSSD_ConnectionPoint, *PTSSD_ConnectionPoint
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
product: Windows
targetos: Windows
req.lib: Setupapi.lib
req.dll: Setupapi.dll
req.irql: 
req.product: ADAM
---

# SetupQueueCopyA function


## -description


<p class="CCE_Message">[This function is available for use in the operating systems indicated in the Requirements section. It may be altered or unavailable in subsequent versions.   SetupAPI should no longer be used for installing applications. Instead, use the Windows Installer for developing application installers. SetupAPI continues to be used for installing device drivers.]

The 
<b>SetupQueueCopy</b> function adds a single file copy operation to a setup file queue.


## -parameters




### -param QueueHandle [in]

Handle to a setup file queue, as returned by 
<a href="https://msdn.microsoft.com/36950f18-80ae-46b7-9f9f-bd5307d72a3b">SetupOpenFileQueue</a>.


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
<a href="https://msdn.microsoft.com/en-us/library/ms646997(v=VS.85).aspx">VS_FIXEDFILEINFO</a> structure, as filled in by the  version functions. If one of the files does not have version resources, or if they have identical version information, the source file is considered newer.

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


## -returns



If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



If a UNC directory is specified as the target directory of a file copy operation, you must ensure it exists before the queue is committed. The setup functions do not check for the existence of and do not create UNC directories. If the target UNC directory does not exist, the file copy will fail.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn938561">Functions</a>



<a href="https://msdn.microsoft.com/58201596-cb8c-480a-abef-896c1f9ef098">Overview</a>



<a href="https://msdn.microsoft.com/f61fd00e-e60f-4722-9da7-1ed4d8491004">SetupQueueCopySection</a>



<a href="https://msdn.microsoft.com/57e8dc72-5b0e-486c-9819-fa44085580eb">SetupQueueDefaultCopy</a>



<a href="https://msdn.microsoft.com/21cdaf05-c4fb-4130-baa5-31baf5391ece">SetupQueueDelete</a>



<a href="https://msdn.microsoft.com/0b80eba9-9e71-4255-8c1b-039878682ec4">SetupQueueRename</a>
 

 

