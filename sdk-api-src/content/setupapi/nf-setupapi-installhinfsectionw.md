---
UID: NF:setupapi.InstallHinfSectionW
title: InstallHinfSectionW function (setupapi.h)
description: InstallHinfSection is an entry-point function exported by Setupapi.dll that you can use to execute a section of an .inf file. InstallHinfSection can be invoked by calling the Rundll32.exe utility as described in the Remarks section. (Unicode)
helpviewer_keywords: ["InstallHinfSection","InstallHinfSection function [Setup API]","InstallHinfSectionA","InstallHinfSectionW","_setupapi_installhinfsection","setup.installhinfsection","setupapi/InstallHinfSection","setupapi/InstallHinfSectionA","setupapi/InstallHinfSectionW"]
old-location: setup\installhinfsection.htm
tech.root: setup
ms.assetid: 151aa91b-9b3d-45e8-94a3-2bc395cd466d
ms.date: 12/05/2018
ms.keywords: InstallHinfSection, InstallHinfSection function [Setup API], InstallHinfSectionA, InstallHinfSectionW, _setupapi_installhinfsection, setup.installhinfsection, setupapi/InstallHinfSection, setupapi/InstallHinfSectionA, setupapi/InstallHinfSectionW
req.header: setupapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: InstallHinfSectionW (Unicode) and InstallHinfSectionA (ANSI)
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
 - InstallHinfSectionW
 - setupapi/InstallHinfSectionW
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
 - InstallHinfSection
 - InstallHinfSectionA
 - InstallHinfSectionW
---

# InstallHinfSectionW function


## -description

<p class="CCE_Message">[This function is available for use in the operating systems indicated in the Requirements section. It may be altered or unavailable in subsequent versions.   SetupAPI should no longer be used for installing applications. Instead, use the Windows Installer for developing application installers. SetupAPI continues to be used for installing device drivers.]

<b>InstallHinfSection</b> is an entry-point function exported by Setupapi.dll that you can use to execute a section of an .inf file. 
<b>InstallHinfSection</b> can be invoked by calling the Rundll32.exe utility as described in the Remarks section.

The prototype for the 
<b>InstallHinfSection</b> function follows the form of all entry-point functions used with Rundll32.exe.

If a file is copied or modified, the caller of this function is required have privileges to write into the target directory. If there are any services being installed, the caller of this function is required have access to the 
<a href="/windows/desktop/Services/service-control-manager">Service Control Manager</a>.

## -parameters

### -param Window [in]

The parent window handle. Typically <i>hwnd</i> is Null.

### -param ModuleHandle [in]

Reserved and should be Null.

### -param CommandLine [in]

Pointer to buffer containing the command line. You should use a null-terminated string.

### -param ShowCommand [in]

Reserved and should be zero.

## -remarks

Note that three exports exist: 
<b>InstallHinfSection</b> (for RunDll32), <b>InstallHinfSectionA</b>, and <b>InstallHinfSectionW</b>. 

To run an <b>Install</b> section of a specified .inf file, you can invoke 
<b>InstallHinfSection</b> with the Rundll32.exe by using the following syntax.

<b>RUNDLL32.EXE SETUPAPI.DLL,InstallHinfSection </b><i>&lt;section&gt;</i><i>&lt;mode&gt;</i><i>&lt;path&gt;</i>

This passes "<i>&lt;section&gt;</i><i>&lt;mode&gt;</i><i>&lt;path&gt;</i>" to <i>CmdLineBuffer</i>.

Alternatively, your program may call 
<b>InstallHinfSection</b>, <b>InstallHinfSectionA</b>, or <b>InstallHinfSectionW</b> directly, setting the <i>CmdLineBuffer</i> parameter to the following.


``` syntax
"<section> <mode> <path>"
```

Where <i>path</i> is the full path to the .inf file, <i>mode</i> is the reboot mode parameter, and <i>section</i> is any <b>Install</b> section in the .inf file. The comma separator between SETUPAPI.DLL and 
<b>InstallHinfSection</b> on the command line is required. Note that there cannot be any white space on the command line between the comma and SETUPAPI.DLL or 
<b>InstallHinfSection</b>.

It is recommended that you specify the full path to the .inf file as <i>path</i>.

You may specify any <b>Install</b> section in the .inf file as <i>section</i>. No spaces are allowed.

You should use a combination of the following values for <i>mode</i>. You must include 128 to set the default path of the installation to the location of the INF, otherwise a system-provided INF is assumed. Add values to specify rebooting. Note that only the values 128 or 132 are recommended, other values may cause the computer to reboot unnecessarily or not reboot when it required.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td>0</td>
<td>System provided INF.</td>
</tr>
<tr>
<td>128</td>
<td>Set the default path of the installation to the location of the INF. This is the typical setting.</td>
</tr>
<tr>
<td>+0</td>
<td>Never reboot the computer.</td>
</tr>
<tr>
<td>+1</td>
<td>Reboot the computer in all cases.</td>
</tr>
<tr>
<td>+2</td>
<td>Always ask the users if they want to reboot.</td>
</tr>
<tr>
<td>+3</td>
<td>Reboot the computer if necessary without asking user for permission.</td>
</tr>
<tr>
<td>+4</td>
<td>If a reboot of the computer is necessary, ask the user for permission before rebooting.</td>
</tr>
</table>
 


<div> </div>


For example, the following command line runs the DefaultInstall section of the Shell.inf file. If Setup determines a reboot is required, the user is will be prompted with a "Reboot the computer, Yes/No" dialog box.

<b>RUNDLL32.EXE SETUPAPI.DLL,InstallHinfSection DefaultInstall 132 C:\WINDOWS\INF\SHELL.INF</b>




> [!NOTE]
> The setupapi.h header defines InstallHinfSection as an alias which automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
