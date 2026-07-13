---
UID: NF:msi.MsiSetInternalUI
title: MsiSetInternalUI function (msi.h)
description: The MsiSetInternalUI function enables the installer's internal user interface. Then this user interface is used for all subsequent calls to user-interface-generating installer functions in this process. For more information, see User Interface Levels.
helpviewer_keywords: ["INSTALLUILEVEL_BASIC","INSTALLUILEVEL_DEFAULT","INSTALLUILEVEL_ENDDIALOG","INSTALLUILEVEL_FULL","INSTALLUILEVEL_HIDECANCEL","INSTALLUILEVEL_NOCHANGE","INSTALLUILEVEL_NONE","INSTALLUILEVEL_PROGRESSONLY","INSTALLUILEVEL_REDUCED","INSTALLUILEVEL_SOURCERESONLY","MsiSetInternalUI","MsiSetInternalUI function","_msi_msisetinternalui","msi/MsiSetInternalUI","setup.msisetinternalui"]
old-location: setup\msisetinternalui.htm
tech.root: setup
ms.assetid: 303c2ea9-4c8f-46d3-b587-7c50e2810c28
ms.date: 12/05/2018
ms.keywords: INSTALLUILEVEL_BASIC, INSTALLUILEVEL_DEFAULT, INSTALLUILEVEL_ENDDIALOG, INSTALLUILEVEL_FULL, INSTALLUILEVEL_HIDECANCEL, INSTALLUILEVEL_NOCHANGE, INSTALLUILEVEL_NONE, INSTALLUILEVEL_PROGRESSONLY, INSTALLUILEVEL_REDUCED, INSTALLUILEVEL_SOURCERESONLY, MsiSetInternalUI, MsiSetInternalUI function, _msi_msisetinternalui, msi/MsiSetInternalUI, setup.msisetinternalui
req.header: msi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7. Windows Installer 4.0 or Windows Installer 4.5 on   Windows Server 2008 or Windows Vista. See the Windows Installer Run-Time Requirements for information about the minimum Windows service pack that is required by a Windows Installer version.
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
req.lib: Msi.lib
req.dll: Msi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MsiSetInternalUI
 - msi/MsiSetInternalUI
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Msi.dll
 - Ext-MS-Win-MSIltCfg-MSI-l1-1-0.dll
 - msiltcfg.dll
 - Ext-MS-Win-MSi-Misc-L1-1-0.dll
api_name:
 - MsiSetInternalUI
---

# MsiSetInternalUI function


## -description

The 
<b>MsiSetInternalUI</b> function enables the installer's internal user interface. Then this user interface is used for all subsequent calls to user-interface-generating installer functions in this process. For more information, see 
<a href="/windows/desktop/Msi/user-interface-levels">User Interface Levels</a>.

## -parameters

### -param dwUILevel [in]

Specifies the level of complexity of the user interface. This parameter can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="INSTALLUILEVEL_FULL"></a><a id="installuilevel_full"></a><dl>
<dt><b>INSTALLUILEVEL_FULL</b></dt>
</dl>
</td>
<td width="60%">
Authored user interface with wizards, progress, and errors.

</td>
</tr>
<tr>
<td width="40%"><a id="INSTALLUILEVEL_REDUCED"></a><a id="installuilevel_reduced"></a><dl>
<dt><b>INSTALLUILEVEL_REDUCED</b></dt>
</dl>
</td>
<td width="60%">
Authored user interface with wizard dialog boxes suppressed.

</td>
</tr>
<tr>
<td width="40%"><a id="INSTALLUILEVEL_BASIC"></a><a id="installuilevel_basic"></a><dl>
<dt><b>INSTALLUILEVEL_BASIC</b></dt>
</dl>
</td>
<td width="60%">
Simple progress and error handling.

</td>
</tr>
<tr>
<td width="40%"><a id="INSTALLUILEVEL_DEFAULT"></a><a id="installuilevel_default"></a><dl>
<dt><b>INSTALLUILEVEL_DEFAULT</b></dt>
</dl>
</td>
<td width="60%">
The installer chooses an appropriate user interface level.

</td>
</tr>
<tr>
<td width="40%"><a id="INSTALLUILEVEL_NONE"></a><a id="installuilevel_none"></a><dl>
<dt><b>INSTALLUILEVEL_NONE</b></dt>
</dl>
</td>
<td width="60%">
Completely silent installation.  This includes suppressing the elevation prompt even if required.  See <b>INSTALLUILEVEL_UACONLY</b> if you would like the user to be able to elevate.

</td>
</tr>
<tr>
<td width="40%"><a id="INSTALLUILEVEL_ENDDIALOG"></a><a id="installuilevel_enddialog"></a><dl>
<dt><b>INSTALLUILEVEL_ENDDIALOG</b></dt>
</dl>
</td>
<td width="60%">
If combined with any above value, the installer displays a modal dialog box at the end of a successful installation or if there has been an error. No dialog box is displayed if the user cancels.

</td>
</tr>
<tr>
<td width="40%"><a id="INSTALLUILEVEL_PROGRESSONLY"></a><a id="installuilevel_progressonly"></a><dl>
<dt><b>INSTALLUILEVEL_PROGRESSONLY</b></dt>
</dl>
</td>
<td width="60%">
If combined with the <b>INSTALLUILEVEL_BASIC</b> value, the installer shows simple progress dialog boxes but does not display any modal dialog boxes or error dialog boxes.

</td>
</tr>
<tr>
<td width="40%"><a id="INSTALLUILEVEL_NOCHANGE"></a><a id="installuilevel_nochange"></a><dl>
<dt><b>INSTALLUILEVEL_NOCHANGE</b></dt>
</dl>
</td>
<td width="60%">
No change in the UI level. However, if <i>phWnd</i> is not Null, the parent window can change.

</td>
</tr>
<tr>
<td width="40%"><a id="INSTALLUILEVEL_HIDECANCEL"></a><a id="installuilevel_hidecancel"></a><dl>
<dt><b>INSTALLUILEVEL_HIDECANCEL</b></dt>
</dl>
</td>
<td width="60%">
If combined with the <b>INSTALLUILEVEL_BASIC</b> value, the installer shows simple progress dialog boxes but does not display a <b>Cancel</b> button on the dialog. This prevents users from canceling the install.

</td>
</tr>
<tr>
<td width="40%"><a id="INSTALLUILEVEL_SOURCERESONLY"></a><a id="installuilevel_sourceresonly"></a><dl>
<dt><b>INSTALLUILEVEL_SOURCERESONLY</b></dt>
</dl>
</td>
<td width="60%">
If this value is combined with the <b>INSTALLUILEVEL_NONE</b> value, the installer displays only the dialog boxes used for source resolution. No other dialog boxes are shown. This value has no effect if the UI level is not <b>INSTALLUILEVEL_NONE</b>. It is used with an external user interface designed to handle all of the UI except for source resolution. In this case, the installer handles source resolution.
 
</td>
</tr>
<td width="40%"><a id="INSTALLUILEVEL_UACONLY"></a><a id="installuilevel_uaconly"></a><dl>
<dt><b>INSTALLUILEVEL_UACONLY</b></dt>
</dl>
</td>
<td width="60%">
If combined with the <b>INSTALLUILEVEL_NONE</b> value, the installation will be completely silent except for the prompt for elevation if it is required.
 
</td>
</tr>
</table>

### -param phWnd [in, out]

Pointer to a window. This window becomes the owner of any user interface created. A pointer to the previous owner of the user interface is returned. If this parameter is null, the owner of the user interface does not change.

## -returns

The previous user interface level is returned. If an invalid <i>dwUILevel </i> is passed, then <b>INSTALLUILEVEL_NOCHANGE</b> is returned.

## -remarks

The 
<b>MsiSetInternalUI</b> function is useful when the installer must display a user interface. For example, if a feature is installed, but the source is a compact disc that must be inserted, the installer prompts the user for the compact disc. Depending on the nature of the installation, the application might also display progress indicators or query the user for information.

When Msi.dll is loaded, the user interface level is set to DEFAULT and the user interface owner is set to 0 (that is, the initial user interface owner is the desktop).

## -see-also

<a href="/windows/desktop/Msi/installer-function-reference">Interface and Logging Functions</a>
