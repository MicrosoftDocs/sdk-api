---
UID: NF:setupapi.SetupInstallServicesFromInfSectionExA
title: SetupInstallServicesFromInfSectionExA function (setupapi.h)
description: The SetupInstallServicesFromInfSectionEx function performs service installation and deletion operations that are specified in the Service Install sections listed in the Service section of an INF file. (ANSI)
helpviewer_keywords: ["SPSVCINST_ASSOCSERVICE", "SPSVCINST_CLOBBER_SECURITY", "SPSVCINST_DELETEEVENTLOGENTRY", "SPSVCINST_NOCLOBBER_DEPENDENCIES", "SPSVCINST_NOCLOBBER_DESCRIPTION", "SPSVCINST_NOCLOBBER_DISPLAYNAME", "SPSVCINST_NOCLOBBER_ERRORCONTROL", "SPSVCINST_NOCLOBBER_LOADORDERGROUP", "SPSVCINST_NOCLOBBER_REQUIREDPRIVILEGES", "SPSVCINST_NOCLOBBER_STARTTYPE", "SPSVCINST_STARTSERVICE", "SPSVCINST_STOPSERVICE", "SPSVCINST_TAGTOFRONT", "SetupInstallServicesFromInfSectionExA", "setupapi/SetupInstallServicesFromInfSectionExA"]
old-location: setup\setupinstallservicesfrominfsectionex.htm
tech.root: setup
ms.assetid: c0bf6442-56dc-41f1-8a21-ff7b92b1ef0f
ms.date: 12/20/2024
ms.keywords: SPSVCINST_ASSOCSERVICE, SPSVCINST_CLOBBER_SECURITY, SPSVCINST_DELETEEVENTLOGENTRY, SPSVCINST_NOCLOBBER_DEPENDENCIES, SPSVCINST_NOCLOBBER_DESCRIPTION, SPSVCINST_NOCLOBBER_DISPLAYNAME, SPSVCINST_NOCLOBBER_ERRORCONTROL, SPSVCINST_NOCLOBBER_LOADORDERGROUP, SPSVCINST_NOCLOBBER_REQUIREDPRIVILEGES, SPSVCINST_NOCLOBBER_STARTTYPE, SPSVCINST_STARTSERVICE, SPSVCINST_STOPSERVICE, SPSVCINST_TAGTOFRONT, SetupInstallServicesFromInfSectionEx, SetupInstallServicesFromInfSectionEx function [Setup API], SetupInstallServicesFromInfSectionExA, SetupInstallServicesFromInfSectionExW, _setupapi_setupinstallservicesfrominfsectionex, setup.setupinstallservicesfrominfsectionex, setupapi/SetupInstallServicesFromInfSectionEx, setupapi/SetupInstallServicesFromInfSectionExA, setupapi/SetupInstallServicesFromInfSectionExW
req.header: setupapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SetupInstallServicesFromInfSectionExW (Unicode) and SetupInstallServicesFromInfSectionExA (ANSI)
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
 - SetupInstallServicesFromInfSectionExA
 - setupapi/SetupInstallServicesFromInfSectionExA
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
 - SetupInstallServicesFromInfSectionEx
 - SetupInstallServicesFromInfSectionExA
 - SetupInstallServicesFromInfSectionExW
---

# SetupInstallServicesFromInfSectionExA function


## -description

<p class="CCE_Message">[This function is available for use in the operating systems indicated in the Requirements section. It may be altered or unavailable in subsequent versions.   SetupAPI should no longer be used for installing applications. Instead, use the Windows Installer for developing application installers. SetupAPI continues to be used for installing device drivers.]

The 
<b>SetupInstallServicesFromInfSectionEx</b> function performs service installation and deletion operations that are specified in the <b>Service Install</b> sections listed in the <b>Service</b> section of an INF file.

A caller of this function is required to have access to the 
<a href="/windows/desktop/Services/service-control-manager">Service Control Manager</a>, and privileges to modify services.

## -parameters

### -param InfHandle [in]

A handle to the INF file that contains the <b>Service</b> section.

### -param SectionName [in]

The name of the <b>Service</b> section to process. You should use a null-terminated string.

### -param Flags [in]

The controls for the installation. 



<table>
<tr>
<th>Flag</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SPSVCINST_TAGTOFRONT"></a><a id="spsvcinst_tagtofront"></a><dl>
<dt><b>SPSVCINST_TAGTOFRONT</b></dt>
<dt>0x001</dt>
</dl>
</td>
<td width="60%">
Move the service tag to the front of its group order list.

</td>
</tr>
<tr>
<td width="40%"><a id="SPSVCINST_ASSOCSERVICE"></a><a id="spsvcinst_assocservice"></a><dl>
<dt><b>SPSVCINST_ASSOCSERVICE</b></dt>
<dt>0x002</dt>
</dl>
</td>
<td width="60%">
AddService section: Mark this service as the function driver for the device being installed.

</td>
</tr>
<tr>
<td width="40%"><a id="SPSVCINST_DELETEEVENTLOGENTRY"></a><a id="spsvcinst_deleteeventlogentry"></a><dl>
<dt><b>SPSVCINST_DELETEEVENTLOGENTRY</b></dt>
<dt>0x004</dt>
</dl>
</td>
<td width="60%">
Delete the event log entry for a specified service.

</td>
</tr>
<tr>
<td width="40%"><a id="SPSVCINST_NOCLOBBER_DISPLAYNAME"></a><a id="spsvcinst_noclobber_displayname"></a><dl>
<dt><b>SPSVCINST_NOCLOBBER_DISPLAYNAME</b></dt>
<dt>0x008</dt>
</dl>
</td>
<td width="60%">
Do not overwrite the display name if one already exists.

</td>
</tr>
<tr>
<td width="40%"><a id="SPSVCINST_NOCLOBBER_STARTTYPE"></a><a id="spsvcinst_noclobber_starttype"></a><dl>
<dt><b>SPSVCINST_NOCLOBBER_STARTTYPE</b></dt>
<dt>0x010</dt>
</dl>
</td>
<td width="60%">
Do not overwrite the start type value if the service already exists.

</td>
</tr>
<tr>
<td width="40%"><a id="SPSVCINST_NOCLOBBER_ERRORCONTROL"></a><a id="spsvcinst_noclobber_errorcontrol"></a><dl>
<dt><b>SPSVCINST_NOCLOBBER_ERRORCONTROL</b></dt>
<dt>0x020</dt>
</dl>
</td>
<td width="60%">
Do not overwrite the error control value if the service already exists.

</td>
</tr>
<tr>
<td width="40%"><a id="SPSVCINST_NOCLOBBER_LOADORDERGROUP"></a><a id="spsvcinst_noclobber_loadordergroup"></a><dl>
<dt><b>SPSVCINST_NOCLOBBER_LOADORDERGROUP</b></dt>
<dt>0x040</dt>
</dl>
</td>
<td width="60%">
Do not overwrite the load order group if it already exists.

</td>
</tr>
<tr>
<td width="40%"><a id="SPSVCINST_NOCLOBBER_DEPENDENCIES"></a><a id="spsvcinst_noclobber_dependencies"></a><dl>
<dt><b>SPSVCINST_NOCLOBBER_DEPENDENCIES</b></dt>
<dt>0x080</dt>
</dl>
</td>
<td width="60%">
Do not overwrite the dependencies list if it already exists.

</td>
</tr>
<tr>
<td width="40%"><a id="SPSVCINST_NOCLOBBER_DESCRIPTION"></a><a id="spsvcinst_noclobber_description"></a><dl>
<dt><b>SPSVCINST_NOCLOBBER_DESCRIPTION</b></dt>
<dt>0x100</dt>
</dl>
</td>
<td width="60%">
AddService section: mark this service as the function driver for the device being installed.

</td>
</tr>
<tr>
<td width="40%"><a id="SPSVCINST_STOPSERVICE"></a><a id="spsvcinst_stopservice"></a><dl>
<dt><b>SPSVCINST_STOPSERVICE</b></dt>
<dt>0x200</dt>
</dl>
</td>
<td width="60%">
DelService section: Stop the associated service specified in the entry before deleting the service.

</td>
</tr>
<tr>
<td width="40%"><a id="SPSVCINST_CLOBBER_SECURITY"></a><a id="spsvcinst_clobber_security"></a><dl>
<dt><b>SPSVCINST_CLOBBER_SECURITY</b></dt>
<dt>0x400</dt>
</dl>
</td>
<td width="60%">
AddService section: Security settings the service are overwritten if the service already exists in the system.

<div class="alert"><b>Note</b>  Available starting with Windows Server 2003 and Windows XP.</div>
<div> </div>
</td>
</tr>
<tr>
<td width="40%"><a id="SPSVCINST_STARTSERVICE"></a><a id="spsvcinst_startservice"></a><dl>
<dt><b>SPSVCINST_STARTSERVICE</b></dt>
<dt>0x800</dt>
</dl>
</td>
<td width="60%">
AddService section: Start the service after the service is installed. This flag cannot be used to start a service that implements a Plug and Play (PnP) function driver or filter driver for a device. Otherwise, this flag can be used to start a user-mode or kernel-mode service that is managed by the Service Control Manager (SCM.)

<div class="alert"><b>Note</b>  Available starting with Windows Server 2008 and Windows Vista.</div>
<div> </div>
</td>
</tr>
<tr>
<td width="40%"><a id="SPSVCINST_NOCLOBBER_REQUIREDPRIVILEGES"></a><a id="spsvcinst_noclobber_requiredprivileges"></a><dl>
<dt><b>SPSVCINST_NOCLOBBER_REQUIREDPRIVILEGES</b></dt>
<dt>0x1000</dt>
</dl>
</td>
<td width="60%">
AddService section: Do not overwrite the given service's required privileges if the service already exists in the system.

<div class="alert"><b>Note</b>  Available starting with Windows Server 2008 R2 and Windows 7.</div>
<div> </div>
</td>
</tr>
</table>

### -param DeviceInfoSet [in]

An optional pointer to a handle to a device information set. For more information, see the DDK <i>Programmer's Guide</i>. (This resource may not be available in some languages 

and countries.)

### -param DeviceInfoData [in]

An optional pointer to  the <b>SP_DEVINFO_DATA</b> structure that provides a context to a specific element in the set that  <i>DeviceInfoSet</i> specifies. For more information, see the DDK <i>Programmer's Guide</i>. (This resource may not be available in some languages and countries.)

### -param Reserved1

Reserved.

### -param Reserved2

Reserved.

## -returns

If the function succeeds, the return value is nonzero.  The function calls <b>SetLastError</b> with ERROR_SUCCESS_REBOOT_REQUIRED  if a reboot of the system is required.

If the function fails, the return value is 0 (zero). To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -see-also

<a href="/windows/desktop/SetupApi/functions">Functions</a>



<a href="/windows/desktop/SetupApi/overview">Overview</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupinstallfilesfrominfsectiona">SetupInstallFilesFromInfSection</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupinstallfrominfsectiona">SetupInstallFromInfSection</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupinstallservicesfrominfsectiona">SetupInstallServicesFromInfSection</a>

## -remarks

> [!NOTE]
> The setupapi.h header defines SetupInstallServicesFromInfSectionEx as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

<b>SetupInstallServicesFromInfSectionEx</b> will log diagnostic information to the [SetupAPI application installation text log](/windows-hardware/drivers/install/setupapi-text-logs). This log file is generally off by default. It can be enabled by modifying the *General logging levels* part of the SetupAPI `LogLevel` value as described at [Setting SetupAPI Logging Levels](/windows-hardware/drivers/install/setting-setupapi-logging-levels). For performance reasons, you should only enable this log file when troubleshooting an issue. When the log file is enabled, you can find it at `%windir%\inf\setupapi.app.log`.
