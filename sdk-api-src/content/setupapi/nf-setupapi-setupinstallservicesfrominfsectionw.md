---
UID: NF:setupapi.SetupInstallServicesFromInfSectionW
title: SetupInstallServicesFromInfSectionW function
author: windows-sdk-content
description: The SetupInstallServicesFromInfSection function performs service installation and deletion operations that are specified in the Service Install sections listed in the Service section of an INF file.
old-location: setup\setupinstallservicesfrominfsection.htm
old-project: SetupApi
ms.assetid: 25a937d3-29f4-46e8-91e5-e956fbe647d7
ms.author: windowssdkdev
ms.date: 06/07/2018
ms.keywords: SPSVCINST_CLOBBER_SECURITY, SPSVCINST_DELETEEVENTLOGENTRY, SPSVCINST_NOCLOBBER_DEPENDENCIES, SPSVCINST_NOCLOBBER_DESCRIPTION, SPSVCINST_NOCLOBBER_DISPLAYNAME, SPSVCINST_NOCLOBBER_ERRORCONTROL, SPSVCINST_NOCLOBBER_LOADORDERGROUP, SPSVCINST_NOCLOBBER_REQUIREDPRIVILEGES, SPSVCINST_NOCLOBBER_STARTTYPE, SPSVCINST_STARTSERVICE, SPSVCINST_STOPSERVICE, SPSVCINST_TAGTOFRONT, SetupInstallServicesFromInfSection, SetupInstallServicesFromInfSection function [Setup API], SetupInstallServicesFromInfSectionA, SetupInstallServicesFromInfSectionW, _setupapi_setupinstallservicesfrominfsection, setup.setupinstallservicesfrominfsection, setupapi/SetupInstallServicesFromInfSection, setupapi/SetupInstallServicesFromInfSectionA, setupapi/SetupInstallServicesFromInfSectionW
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
req.unicode-ansi: SetupInstallServicesFromInfSectionW (Unicode) and SetupInstallServicesFromInfSectionA (ANSI)
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
 - Ext-MS-Win-SetupAPI-Inf-L1-1-1.dll
 - Ext-MS-Win-SetupAPI-ClassInstallers-L1-1-2.dll
api_name:
 - SetupInstallServicesFromInfSection
 - SetupInstallServicesFromInfSectionA
 - SetupInstallServicesFromInfSectionW
product: Windows
targetos: Windows
req.lib: Setupapi.lib
req.dll: Setupapi.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# SetupInstallServicesFromInfSectionW function


## -description


<p class="CCE_Message">[This function is available for use in the operating systems indicated in the 
    Requirements section. It may be altered or unavailable in subsequent versions. SetupAPI should no longer be used 
    for installing applications. Instead, use the Windows Installer for developing application installers. SetupAPI 
    continues to be used for installing device drivers.]

The 
    <b>SetupInstallServicesFromInfSection</b> 
    function performs service installation and deletion operations that are specified in the 
    <b>Service Install</b> sections listed in the <b>Service</b> section of 
    an INF file.

A caller of this function is required to have access to the 
    <a href="https://msdn.microsoft.com/56ad011d-17c4-4410-b598-6ef47fb3638f">Service Control Manager</a>, and privileges to modify 
    services.


## -parameters




### -param InfHandle [in]

A handle to the INF file that contains the <b>Service</b> section.


### -param SectionName [in]

The name of the <b>Service</b> section to process. You should use a null-terminated 
      string.


### -param Flags [in]

The controls for the installation of each service in the specified section.

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
AddService section: move the service tag to the front of its group order list.

</td>
</tr>
<tr>
<td width="40%"><a id="SPSVCINST_DELETEEVENTLOGENTRY"></a><a id="spsvcinst_deleteeventlogentry"></a><dl>
<dt><b>SPSVCINST_DELETEEVENTLOGENTRY</b></dt>
<dt>0x004</dt>
</dl>
</td>
<td width="60%">
DelService section: delete the event log entry.

</td>
</tr>
<tr>
<td width="40%"><a id="SPSVCINST_NOCLOBBER_DISPLAYNAME"></a><a id="spsvcinst_noclobber_displayname"></a><dl>
<dt><b>SPSVCINST_NOCLOBBER_DISPLAYNAME</b></dt>
<dt>0x008</dt>
</dl>
</td>
<td width="60%">
AddService section: do not overwrite the display name if one already exists.

</td>
</tr>
<tr>
<td width="40%"><a id="SPSVCINST_NOCLOBBER_STARTTYPE"></a><a id="spsvcinst_noclobber_starttype"></a><dl>
<dt><b>SPSVCINST_NOCLOBBER_STARTTYPE</b></dt>
<dt>0x010</dt>
</dl>
</td>
<td width="60%">
AddService section: do not overwrite the start type value if the service already exists.

</td>
</tr>
<tr>
<td width="40%"><a id="SPSVCINST_NOCLOBBER_ERRORCONTROL"></a><a id="spsvcinst_noclobber_errorcontrol"></a><dl>
<dt><b>SPSVCINST_NOCLOBBER_ERRORCONTROL</b></dt>
<dt>0x020</dt>
</dl>
</td>
<td width="60%">
AddService section: do not overwrite the error control value if the service already exists.

</td>
</tr>
<tr>
<td width="40%"><a id="SPSVCINST_NOCLOBBER_LOADORDERGROUP"></a><a id="spsvcinst_noclobber_loadordergroup"></a><dl>
<dt><b>SPSVCINST_NOCLOBBER_LOADORDERGROUP</b></dt>
<dt>0x040</dt>
</dl>
</td>
<td width="60%">
AddService section: do not overwrite the load order group if it already exists.

</td>
</tr>
<tr>
<td width="40%"><a id="SPSVCINST_NOCLOBBER_DEPENDENCIES"></a><a id="spsvcinst_noclobber_dependencies"></a><dl>
<dt><b>SPSVCINST_NOCLOBBER_DEPENDENCIES</b></dt>
<dt>0x080</dt>
</dl>
</td>
<td width="60%">
AddService section: do not overwrite the dependencies list if it already exists.

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
AddService section: Security settings the service are overwritten if the service already exists in the 
         system.

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
AddService section: Start the service after the service is installed. This flag cannot be used to start a 
         service that implements a Plug and Play (PnP) function driver or filter driver for a device. Otherwise, 
         this flag can be used to start a user-mode or kernel-mode service that is managed by the Service Control 
         Manager (SCM.)

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
AddService section: Do not overwrite the given service's required privileges if the service already exists 
         in the system.

<div class="alert"><b>Note</b>  Available starting with Windows Server 2008 R2 and Windows 7.</div>
<div> </div>
</td>
</tr>
</table>
 


## -returns



If the function succeeds, the return value is nonzero. The function calls 
       <b>SetLastError</b> with ERROR_SUCCESS_REBOOT_REQUIRED if a reboot of the system is 
       required.

If the function fails, the return value is 0 (zero). To get extended error information, call 
       <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn938561">Functions</a>



<a href="https://msdn.microsoft.com/58201596-cb8c-480a-abef-896c1f9ef098">Overview</a>



<a href="https://msdn.microsoft.com/9834a3b0-f8f5-4e4d-92b2-d3c5a4939a41">SetupInstallFilesFromInfSection</a>



<a href="https://msdn.microsoft.com/bd1ee91a-b58b-4f08-9181-42fbe9d763f9">SetupInstallFromInfSection</a>



<a href="https://msdn.microsoft.com/c0bf6442-56dc-41f1-8a21-ff7b92b1ef0f">SetupInstallServicesFromInfSectionEx</a>
 

 

