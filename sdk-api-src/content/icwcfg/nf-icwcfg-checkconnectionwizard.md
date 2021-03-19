---
UID: NF:icwcfg.CheckConnectionWizard
title: CheckConnectionWizard function (icwcfg.h)
description: The CheckConnectionWizard function checks that the Internet Connection Wizard (ICW) is installed and that it has not been run before.
helpviewer_keywords: ["CheckConnectionWizard","CheckConnectionWizard function [Windows API]","ICW_ALREADYRUN","ICW_CHECKSTATUS","ICW_FULLPRESENT","ICW_FULL_SMARTSTART","ICW_LAUNCHEDFULL","ICW_LAUNCHEDMANUAL","ICW_LAUNCHFULL","ICW_LAUNCHMANUAL","ICW_MANUALPRESENT","ICW_USE_SHELLNEXT","icwcfg/CheckConnectionWizard","winprog.checkconnectionwizard"]
old-location: winprog\checkconnectionwizard.htm
tech.root: winprog
ms.assetid: 81960d59-3de3-4d86-948e-939c59073bb1
ms.date: 12/05/2018
ms.keywords: CheckConnectionWizard, CheckConnectionWizard function [Windows API], ICW_ALREADYRUN, ICW_CHECKSTATUS, ICW_FULLPRESENT, ICW_FULL_SMARTSTART, ICW_LAUNCHEDFULL, ICW_LAUNCHEDMANUAL, ICW_LAUNCHFULL, ICW_LAUNCHMANUAL, ICW_MANUALPRESENT, ICW_USE_SHELLNEXT, icwcfg/CheckConnectionWizard, winprog.checkconnectionwizard
req.header: icwcfg.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Inetcfg.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CheckConnectionWizard
 - icwcfg/CheckConnectionWizard
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Inetcfg.dll
api_name:
 - CheckConnectionWizard
---

# CheckConnectionWizard function


## -description

<p class="CCE_Message">[This function is unsupported and may be altered or unavailable in future  versions of Windows.  ]

The <b>CheckConnectionWizard</b> function checks that the Internet Connection Wizard (ICW) is installed  and that it has not been run
            before.  <b>CheckConnectionWizard</b> then either runs the  ICW or returns the status of the ICW as specified by  the run flags provided and the status of any previous run of the ICW.

## -parameters

### -param unnamedParam1

A combination of bit flags that indicates the action <b>CheckConnectionWizard</b> is to perform.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="ICW_CHECKSTATUS"></a><a id="icw_checkstatus"></a><dl>
<dt><b>ICW_CHECKSTATUS</b></dt>
<dt>0x0001</dt>
</dl>
</td>
<td width="60%">
Check if the ICW is present and if it
                                    has been run.

</td>
</tr>
<tr>
<td width="40%"><a id="ICW_LAUNCHFULL"></a><a id="icw_launchfull"></a><dl>
<dt><b>ICW_LAUNCHFULL</b></dt>
<dt>0x0100</dt>
</dl>
</td>
<td width="60%">
Check if the ICW is present and the retail mode ISP signup
                                    is available and, if
                                    possible, run the ICW.

</td>
</tr>
<tr>
<td width="40%"><a id="ICW_LAUNCHMANUAL"></a><a id="icw_launchmanual"></a><dl>
<dt><b>ICW_LAUNCHMANUAL</b></dt>
<dt>0x0200</dt>
</dl>
</td>
<td width="60%">
Check if the ICW is present, run the ICW in Internet Explorer Administrator Kit (IEAK) Kiosk mode.

</td>
</tr>
<tr>
<td width="40%"><a id="_ICW_USE_SHELLNEXT"></a><a id="_icw_use_shellnext"></a><dl>
<dt><b> ICW_USE_SHELLNEXT</b></dt>
<dt>0x0400</dt>
</dl>
</td>
<td width="60%">
 If the retail mode ISP signup is present, run the ICW using the value set in the <b>ShellNext</b> registry key by <a href="/windows/desktop/api/icwcfg/nf-icwcfg-setshellnext">SetShellNext</a> function.

</td>
</tr>
<tr>
<td width="40%"><a id="ICW_FULL_SMARTSTART"></a><a id="icw_full_smartstart"></a><dl>
<dt><b>ICW_FULL_SMARTSTART</b></dt>
<dt>0x800</dt>
</dl>
</td>
<td width="60%">
If the ICW is present, the retail mode ISP signup 
                                    is available, and <b>ICW_LAUNCHFULL</b> is
                                    specified, run the ICW with the <i>smartstart</i> command line parameter.

</td>
</tr>
</table>

### -param unnamedParam2

<b>DWORD</b> in which the results of the call are returned.  The value is  a
                combination of the following bit flags.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="ICW_FULLPRESENT"></a><a id="icw_fullpresent"></a><dl>
<dt><b>ICW_FULLPRESENT</b></dt>
<dt>0x0001</dt>
</dl>
</td>
<td width="60%">
The retail mode ISP signup  is present on the system.

</td>
</tr>
<tr>
<td width="40%"><a id="ICW_MANUALPRESENT"></a><a id="icw_manualpresent"></a><dl>
<dt><b>ICW_MANUALPRESENT</b></dt>
<dt>0x0002</dt>
</dl>
</td>
<td width="60%">
IEAK mode is present.  This is
                                    always  set if <b>ICW_FULLPRESENT</b> is set.

</td>
</tr>
<tr>
<td width="40%"><a id="ICW_ALREADYRUN"></a><a id="icw_alreadyrun"></a><dl>
<dt><b>ICW_ALREADYRUN</b></dt>
<dt>0x0004</dt>
</dl>
</td>
<td width="60%">
The ICW has been previously run to completion.

</td>
</tr>
<tr>
<td width="40%"><a id="ICW_LAUNCHEDFULL"></a><a id="icw_launchedfull"></a><dl>
<dt><b>ICW_LAUNCHEDFULL</b></dt>
<dt>0x0100</dt>
</dl>
</td>
<td width="60%">
The retail mode ISP signup  ICW was started.

</td>
</tr>
<tr>
<td width="40%"><a id="ICW_LAUNCHEDMANUAL"></a><a id="icw_launchedmanual"></a><dl>
<dt><b>ICW_LAUNCHEDMANUAL</b></dt>
<dt>0x0200</dt>
</dl>
</td>
<td width="60%">
The IEAK mode of ICW was started.

</td>
</tr>
</table>

## -returns

<b>ERROR_SUCCESS</b> indicates a successful call.
            Any other value indicates failure.

## -remarks

If the ICW is present but has not been run to completion, <b>CheckConnectionWizard</b> does one of
            the following based on the value of <i>dwRunFlags</i>:  returns, runs
            the full ICW in retail mode ISP signup, or runs ICW in the IEAK mode.

The retail mode ISP signup  is run using Icwconn1.exe. IEAK mode is run using Isign32.exe.

<div class="alert"><b>Note</b>   The calling application should exit if <b>ICW_LAUNCHEDFULL</b> or
                    <b>ICW_LAUNCHEDMANUAL</b> is set.  The ICW may cause the system to
                    reboot if required system software needs to be installed.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/icwcfg/nf-icwcfg-setshellnext">SetShellNext</a>