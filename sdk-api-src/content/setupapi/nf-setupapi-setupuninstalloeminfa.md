---
UID: NF:setupapi.SetupUninstallOEMInfA
title: SetupUninstallOEMInfA function (setupapi.h)
description: The SetupUninstallOEMInf function uninstalls a specified .inf file and any associated .pnf file. (ANSI)
helpviewer_keywords: ["SUOI_FORCEDELETE", "SetupUninstallOEMInfA", "setupapi/SetupUninstallOEMInfA"]
old-location: setup\setupuninstalloeminf.htm
tech.root: setup
ms.assetid: 70cec8c7-7954-44d7-93f5-711368f72bf7
ms.date: 10/25/2022
ms.keywords: SUOI_FORCEDELETE, SetupUninstallOEMInf, SetupUninstallOEMInf function [Setup API], SetupUninstallOEMInfA, SetupUninstallOEMInfW, _setupapi_setupuninstalloeminf, setup.setupuninstalloeminf, setupapi/SetupUninstallOEMInf, setupapi/SetupUninstallOEMInfA, setupapi/SetupUninstallOEMInfW
req.header: setupapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SetupUninstallOEMInfW (Unicode) and SetupUninstallOEMInfA (ANSI)
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
 - SetupUninstallOEMInfA
 - setupapi/SetupUninstallOEMInfA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Setupapi.dll
 - Ext-MS-Win-SetupAPI-ClassInstallers-L1-1-2.dll
api_name:
 - SetupUninstallOEMInf
 - SetupUninstallOEMInfA
 - SetupUninstallOEMInfW
req.apiset: ext-ms-win-setupapi-classinstallers-l1-1-2 (introduced in Windows 10, version 10.0.14393)
---

# SetupUninstallOEMInfA function


## -description

<p class="CCE_Message">[This function is available for use in the operating systems indicated in the Requirements section. It may be altered or unavailable in subsequent versions.   SetupAPI should no longer be used for installing applications. Instead, use the Windows Installer for developing application installers. SetupAPI continues to be used for installing device drivers.]

The 
<b>SetupUninstallOEMInf</b> function uninstalls a specified .inf file and any associated .pnf file. If the .inf file was installed with a catalog for signing drivers, the catalog is also removed. A caller of this function must have administrative privileges, otherwise the function fails.

## -parameters

### -param InfFileName [in]

File name, without path, of the .inf file in the Windows Inf directory that is to be uninstalled.

### -param Flags [in]

This parameter can be set as follows.

<table>
<tr>
<th>Flag</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SUOI_FORCEDELETE"></a><a id="suoi_forcedelete"></a><dl>
<dt><b>SUOI_FORCEDELETE</b></dt>
<dt>0x0001</dt>
</dl>
</td>
<td width="60%">
The <b>SetupUninstallOEMInf</b> function first checks whether there are any devices installed using the .inf file. A device does not need to be  present to be detected as using the .inf file.

If this flag is not set and the function finds a currently installed device that was installed using this .inf file, the .inf file is not removed.

If this flag is set, the .inf file is removed whether  the function finds a device that was installed with this .inf file.

<div class="alert"><b>Note</b>  This flag only applies to x86, amd64, and ia64 architectures.  It is ignored on all other architectures.</div>
<div> </div>
<div class="alert"><b>Note</b>  If the driver package has any files that are copied to a <a href="/windows-hardware/drivers/install/inf-destinationdirs-section">DestinationDir</a> that uses a <a href="/windows-hardware/drivers/install/using-dirids">DirId</a> of 13, then this force flag is ignored.</div>
<div> </div>
<div class="alert"><b>Note</b>  It is recommended to use <a href="/windows/win32/api/newdev/nf-newdev-diuninstalldrivera">DiUninstallDriver</a> to remove a driver package instead of using this flag.</div>
<div> </div>
</td>
</tr>
</table>

### -param Reserved [in]

Set to <b>null</b>.

## -returns

This function returns WINSETUPAPI BOOL.

## -see-also

<a href="/windows/desktop/SetupApi/functions">Functions</a>


<a href="/windows/desktop/SetupApi/overview">Overview</a>


<a href="/windows/desktop/api/setupapi/nf-setupapi-setupcopyoeminfa">SetupCopyOEMInf</a>


<a href="/windows/win32/api/newdev/nf-newdev-diuninstalldrivera">DiUninstallDriver</a>

## -remarks

> [!NOTE]
> The setupapi.h header defines SetupUninstallOEMInf as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
