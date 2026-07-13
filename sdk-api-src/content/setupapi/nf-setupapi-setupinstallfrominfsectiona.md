---
UID: NF:setupapi.SetupInstallFromInfSectionA
title: SetupInstallFromInfSectionA function (setupapi.h)
description: The SetupInstallFromInfSection function carries out all the directives in an INF file Install section. (ANSI)
helpviewer_keywords: ["SetupInstallFromInfSectionA", "setupapi/SetupInstallFromInfSectionA"]
old-location: setup\setupinstallfrominfsection.htm
tech.root: setup
ms.assetid: bd1ee91a-b58b-4f08-9181-42fbe9d763f9
ms.date: 12/20/2024
ms.keywords: SetupInstallFromInfSection, SetupInstallFromInfSection function [Setup API], SetupInstallFromInfSectionA, SetupInstallFromInfSectionW, _setupapi_setupinstallfrominfsection, setup.setupinstallfrominfsection, setupapi/SetupInstallFromInfSection, setupapi/SetupInstallFromInfSectionA, setupapi/SetupInstallFromInfSectionW
req.header: setupapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SetupInstallFromInfSectionW (Unicode) and SetupInstallFromInfSectionA (ANSI)
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
 - SetupInstallFromInfSectionA
 - setupapi/SetupInstallFromInfSectionA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Setupapi.dll
 - Ext-MS-Win-SetupAPI-Inf-L1-1-1.dll
 - Ext-MS-Win-SetupAPI-ClassInstallers-L1-1-2.dll
api_name:
 - SetupInstallFromInfSection
 - SetupInstallFromInfSectionA
 - SetupInstallFromInfSectionW
req.apiset: ext-ms-win-setupapi-classinstallers-l1-1-2 (introduced in Windows 10, version 10.0.14393)
---

# SetupInstallFromInfSectionA function


## -description

<p class="CCE_Message">[This function is available for use in the operating systems indicated in the 
    Requirements section. It may be altered or unavailable in subsequent versions. SetupAPI should no longer be used 
    for installing applications. Instead, use the Windows Installer for developing application installers. SetupAPI 
    continues to be used for installing device drivers.]

The <b>SetupInstallFromInfSection</b> function carries out all the directives in an 
    INF file <b>Install</b> section.

If the registry or file is modified, the caller of this function is required have privileges to write into the 
    system or target directory.

## -parameters

### -param Owner

Optional pointer to the window handle to the window that owns any dialog boxes that are generated during 
      installation, such as for disk prompting or file copying. If <i>Owner</i> is not specified, 
      these dialog boxes become top-level windows.

### -param InfHandle

Handle to the INF file that contains the section to be processed.

### -param SectionName

Name of the <b>Install</b> section in the INF file to process.

### -param Flags

Controls what actions to perform. The flags can be a combination of the following values.





#### SPINST_INIFILES

Perform INI-file operations (<b>UpdateInis</b>, 
         <b>UpdateIniFields</b> lines in the Install section being processed).



#### SPINST_REGISTRY

Perform registry operations (<b>AddReg</b>, <b>DelReg</b> 
        lines in the <b>Install</b> section being processed).



#### SPINST_INI2REG

Perform INI-file to registry operations (<b>Ini2Reg</b> lines in the <b>Install</b> section being 
         processed).



#### SPINST_LOGCONFIG

This flag is only used when installing a device driver.

Perform logical configuration operations (<b>LogConf</b> lines in the 
          <b>Install</b> section being processed). This flag is only used if 
          <i>DeviceInfoSet</i> and <i>DeviceInfoData</i> are specified.

For more information about installing device drivers, <b>LogConf</b>, 
          <i>DeviceInfoSet</i>, or <i>DeviceInfoData</i>, see the 
          DDK <i>Programmer's Guide</i>.



#### SPINST_FILES

Perform file operations (<b>CopyFiles</b>, <b>DelFiles</b>, <b>RenFiles</b> lines in the 
         <b>Install</b> section being processed).



#### SPINST_ALL

Perform all installation operations.



#### SPINST_REGISTERCALLBACKAWARE

When using the <b>RegisterDlls</b> INF directive to self-register DLLs 
         on Windows 2000, callers of <b>SetupInstallFromInfSection</b> may 
         receive notifications on each file as it is registered or unregistered. To send a 
         <a href="/windows/desktop/SetupApi/spfilenotify-startregistration">SPFILENOTIFY_STARTREGISTRATION</a> or 
         <a href="/windows/desktop/SetupApi/spfilenotify-endregistration">SPFILENOTIFY_ENDREGISTRATION</a> 
         notification to the callback routine, include SPINST_REGISTERCALLBACKAWARE plus either SPINST_REGSVR or 
         SPINST_UNREGSVR. The caller must also set the <i>MsgHandler</i> parameter.



#### SPINST_REGSVR

To send a notification to the callback routine when registering a file, include 
         SPINST_REGISTERCALLBACKAWARE plus SPINST_REGSVR in <i>Flags</i>. The caller must also 
         specify the <i>MsgHandler</i> parameter.



#### SPINST_UNREGSVR

To send a notification to the callback routine when unregistering a file, include 
         SPINST_REGISTERCALLBACKAWARE plus SPINST_UNREGSVR in the <i>Flags</i>. The caller must 
         also specify the <i>MsgHandler</i> parameter.

### -param RelativeKeyRoot

Optional parameter that must be specified if <i>Flags</i> includes SPINST_REGISTRY or 
      SPINST_INI2REG. Handle to a registry key to be used as the root when the INF file specifies HKR as the key. 
      Note that this parameter is ignored if <b>SetupInstallFromInfSection</b> is called 
      with the optional <i>DeviceInfoSet</i> and <i>DeviceInfoData</i> set.

### -param SourceRootPath

Source root for file copies. An example would be A:\ or \\pegasus\win\install. If 
      <i>Flags</i> includes SPINST_FILES, and <i>SourceRootPath</i> is NULL, 
      the system provides a default root path.

### -param CopyFlags

Optional parameter that must be specified if <i>Flags</i> includes SPINST_FILES. 
       Specifies flags to be passed to the 
       <a href="/windows/desktop/api/setupapi/nf-setupapi-setupqueuecopysectiona">SetupQueueCopySection</a> function when files 
       are queued for copy. These flags may be a combination of the following values.





#### SP_COPY_DELETESOURCE

Delete the source file upon successful copy. The caller is not notified if the delete fails.



#### SP_COPY_REPLACEONLY

Copy the file only if doing so would overwrite a file at the destination path.



#### SP_COPY_NEWER_OR_SAME

Examine each file being copied to see if its version resources indicate that it is either the same 
          version or not newer than an existing copy on the target.

The file version information used during version checks is that specified in the 
          <b>dwFileVersionMS</b> and <b>dwFileVersionLS</b> members of a 
          <a href="/windows/desktop/api/verrsrc/ns-verrsrc-vs_fixedfileinfo">VS_FIXEDFILEINFO</a> structure, as filled 
          in by the  version functions. If one of the files does not have version resources, or if they have 
          identical version information, the source file is considered newer.

If the source file is not equal in version or newer, and <i>CopyMsgHandler</i> is 
          specified, the caller is notified and may cancel the copy. If <i>CopyMsgHandler</i> is 
          not specified, the file is not copied.



#### SP_COPY_NEWER_ONLY

Examine each file being copied to see if its version resources indicate that it is not newer than an 
         existing copy on the target. If the source file is newer but not equal in version to the existing target, 
         the file is copied.



#### SP_COPY_NOOVERWRITE

Check whether the target file exists, and, if so, notify the caller who may veto the copy. If 
         <i>CopyMsgHandler</i> is not specified, the file is not overwritten.



#### SP_COPY_NODECOMP

Do not decompress the file. When this flag is set, the target file is not given the uncompressed form 
         of the source name (if appropriate). For example, copying f:/x86\cmd.ex_ to 
         \\install\temp results in a target file of \\install\temp\cmd.ex_. If the 
         SP_COPY_NODECOMP flag was not specified, the file would be decompressed and the target would be called 
         \\install\temp\cmd.exe. The filename part of <i>DestinationName</i>, if 
         specified, is stripped and replaced with the filename of the source file. When SP_COPY_NODECOMP is 
         specified, no language or version information can be checked.



#### SP_COPY_LANGUAGEAWARE

Examine each file being copied to see if its language differs from the language of any existing file 
         already on the target. If so, and <i>CopyMsgHandler</i> is specified, the caller is 
         notified and may cancel the copy. If <i>CopyMsgHandler</i> is not specified, the file is 
         not copied.



#### SP_COPY_SOURCE_ABSOLUTE

<i>SourceFile</i> is a full source path. Do not look it up in the 
          <b>SourceDisksNames</b> section of the INF file.



#### SP_COPY_SOURCEPATH_ABSOLUTE

<i>SourcePathRoot</i> is the full path part of the source file. Ignore the relative 
          source specified in the <b>SourceDisksNames</b> section of the INF file for 
          the source media where the file is located. This flag is ignored if SP_COPY_SOURCE_ABSOLUTE is 
          specified.



#### SP_COPY_FORCE_IN_USE

If the target exists, behave as if it is in use and queue the file for copying on the next system 
         reboot.



#### SP_COPY_IN_USE_NEEDS_REBOOT

If the file was in use during the copy operation inform the user that the system needs to be rebooted. 
         This flag is only used when later calling 
         <a href="/windows/desktop/api/setupapi/nf-setupapi-setuppromptreboot">SetupPromptReboot</a> or 
         <a href="/windows/desktop/api/setupapi/nf-setupapi-setupscanfilequeuea">SetupScanFileQueue</a>.



#### SP_COPY_NOSKIP

Do not give the user the option to skip a file.



#### SP_COPY_FORCE_NOOVERWRITE

Check whether the target file exists, and, if so, the file is not overwritten. The caller is not 
         notified.



#### SP_COPY_FORCE_NEWER

Examine each file being copied to see if its version resources (or time stamps for non-image files) 
         indicate that it is not newer than an existing copy on the target. If the file being copied is not newer, 
         the file is not copied. The caller is not notified.



#### SP_COPY_WARNIFSKIP

If the user tries to skip a file, warn them that skipping a file may affect the installation. (Used for 
         system-critical files.)

### -param MsgHandler

Pointer to the callback routine. The callback routine must be in the format of 
       <a href="/windows/desktop/api/setupapi/nc-setupapi-psp_file_callback_a">FileCallback</a>. See 
       <a href="/windows/desktop/SetupApi/notifications">Notifications</a> for more information.

This parameter is optional only if the <i>Flags</i> parameter does not include 
       SPINST_FILES, SPINST_REGISTERCALLBACKAWARE plus SPINST_REGSVR, or SPINST_UNREGSVR.

<i>MsgHandler</i> must be set if <i>Flags</i> includes SPINST_FILES. In 
       this case, notification is sent to the callback routine when the file queue is committed with 
       <a href="/windows/desktop/api/setupapi/nf-setupapi-setupcommitfilequeuea">SetupCommitFileQueue</a>.

<i>MsgHandler</i> must be set if <i>Flags</i> includes 
        SPINST_REGISTERCALLBACKAWARE plus SPINST_REGSVR or SPINST_UNREGSVR. In this case a 
        <a href="/windows/desktop/SetupApi/spfilenotify-startregistration">SPFILENOTIFY_STARTREGISTRATION</a> 
        or 
        <a href="/windows/desktop/SetupApi/spfilenotify-endregistration">SPFILENOTIFY_ENDREGISTRATION</a> 
        is sent to the callback routine once each time a file is registered or unregistered using the 
        <b>RegisterDlls</b> INF directive on Windows 2000.

### -param Context

Value to be passed to the callback function when the file queue built by this routine internally is 
      committed via 
      <a href="/windows/desktop/api/setupapi/nf-setupapi-setupcommitfilequeuea">SetupCommitFileQueue</a>. The 
      <i>Context</i> parameter is optional only if the <i>Flags</i> parameter 
      does not include SPINST_FILES. This parameter must be specified if <i>Flags</i> includes 
      SPINST_FILES.

### -param DeviceInfoSet

Optional pointer to a handle to a device information set. For more information about 
      the Device Installer setup functions, see the DDK 
      <i>Programmer's Guide</i>.

### -param DeviceInfoData

Optional pointer to a pointer to the <b>SP_DEVINFO_DATA</b> 
      structure that provides a context to a specific element in the set specified by 
      <i>DeviceInfoSet.</i> For more information about the Device Installer setup functions, see 
      the DDK <i>Programmer's Guide</i>.

## -returns

If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero. To get extended error information, call 
       <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

If a UNC directory is specified as the target directory of a file copy operation, you must ensure it exists 
    before you call <b>SetupInstallFromInfSection</b>. The setup functions do not check for 
    the existence of and do not create UNC directories. If the target UNC directory does not exist, the file 
    installation will fail.

This function requires a Windows INF file. Some older INF file  formats may not be supported. 





> [!NOTE]
> The setupapi.h header defines SetupInstallFromInfSection as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

<b>SetupInstallFromInfSection</b> will log diagnostic information to the [SetupAPI application installation text log](/windows-hardware/drivers/install/setupapi-text-logs). This log file is generally off by default. It can be enabled by modifying the *General logging levels* part of the SetupAPI `LogLevel` value as described at [Setting SetupAPI Logging Levels](/windows-hardware/drivers/install/setting-setupapi-logging-levels). For performance reasons, you should only enable this log file when troubleshooting an issue. When the log file is enabled, you can find it at `%windir%\inf\setupapi.app.log`.

## -see-also

<a href="/windows/desktop/SetupApi/functions">Functions</a>



<a href="/windows/desktop/SetupApi/overview">Overview</a>



<a href="/windows/desktop/SetupApi/spfilenotify-endregistration">SPFILENOTIFY_ENDREGISTRATION</a>



<a href="/windows/desktop/SetupApi/spfilenotify-startregistration">SPFILENOTIFY_STARTREGISTRATION</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupinstallservicesfrominfsectiona">SetupInstallServicesFromInfSection</a>
