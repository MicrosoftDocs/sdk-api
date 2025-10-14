---
UID: NF:msi.MsiSetExternalUIA
title: MsiSetExternalUIA function (msi.h)
description: The MsiSetExternalUI function enables an external user-interface handler. (ANSI)
helpviewer_keywords: ["INSTALLLOGMODE_ACTIONDATA", "INSTALLLOGMODE_ACTIONSTART", "INSTALLLOGMODE_COMMONDATA", "INSTALLLOGMODE_ERROR", "INSTALLLOGMODE_FATALEXIT", "INSTALLLOGMODE_FILESINUSE", "INSTALLLOGMODE_INFO", "INSTALLLOGMODE_INITIALIZE", "INSTALLLOGMODE_INSTALLEND", "INSTALLLOGMODE_INSTALLSTART", "INSTALLLOGMODE_OUTOFDISKSPACE", "INSTALLLOGMODE_PROGRESS", "INSTALLLOGMODE_RESOLVESOURCE", "INSTALLLOGMODE_RMFILESINUSE", "INSTALLLOGMODE_SHOWDIALOG", "INSTALLLOGMODE_TERMINATE", "INSTALLLOGMODE_USER", "INSTALLLOGMODE_WARNING", "MsiSetExternalUIA", "msi/MsiSetExternalUIA"]
old-location: setup\msisetexternalui.htm
tech.root: setup
ms.assetid: fcbf0607-d048-486f-bec2-f6e9d03e4194
ms.date: 12/05/2018
ms.keywords: INSTALLLOGMODE_ACTIONDATA, INSTALLLOGMODE_ACTIONSTART, INSTALLLOGMODE_COMMONDATA, INSTALLLOGMODE_ERROR, INSTALLLOGMODE_FATALEXIT, INSTALLLOGMODE_FILESINUSE, INSTALLLOGMODE_INFO, INSTALLLOGMODE_INITIALIZE, INSTALLLOGMODE_INSTALLEND, INSTALLLOGMODE_INSTALLSTART, INSTALLLOGMODE_OUTOFDISKSPACE, INSTALLLOGMODE_PROGRESS, INSTALLLOGMODE_RESOLVESOURCE, INSTALLLOGMODE_RMFILESINUSE, INSTALLLOGMODE_SHOWDIALOG, INSTALLLOGMODE_TERMINATE, INSTALLLOGMODE_USER, INSTALLLOGMODE_WARNING, MsiSetExternalUI, MsiSetExternalUI function, MsiSetExternalUIA, MsiSetExternalUIW, _msi_msisetexternalui, msi/MsiSetExternalUI, msi/MsiSetExternalUIA, msi/MsiSetExternalUIW, setup.msisetexternalui
req.header: msi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7. Windows Installer 4.0 or Windows Installer 4.5 on   Windows Server 2008 or Windows Vista. Windows Installer on Windows Server 2003 or Windows XP. See the Windows Installer Run-Time Requirements for information about the minimum Windows service pack that is required by a Windows Installer version.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: MsiSetExternalUIW (Unicode) and MsiSetExternalUIA (ANSI)
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
 - MsiSetExternalUIA
 - msi/MsiSetExternalUIA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Msi.dll
api_name:
 - MsiSetExternalUI
 - MsiSetExternalUIA
 - MsiSetExternalUIW
---

# MsiSetExternalUIA function


## -description

The 
<b>MsiSetExternalUI</b> function enables an external user-interface handler. This external UI handler is called before the normal internal user-interface handler. The external UI handler has the option to suppress the internal UI by returning a non-zero value to indicate that it has handled the messages. For more information, see 
<a href="/windows/desktop/Msi/about-the-user-interface">About the User Interface</a>.

## -parameters

### -param puiHandler [in]

Specifies a callback function that conforms to the 
<a href="/windows/desktop/api/msi/nc-msi-installui_handlera">INSTALLUI_HANDLER</a> specification.

### -param dwMessageFilter [in]

Specifies which messages to handle using the external message handler. If the external handler returns a non-zero result, then that message will not be sent to the UI, instead the message will be logged if logging has been enabled. For more information, see 
the <a href="/windows/desktop/api/msi/nf-msi-msienableloga">MsiEnableLog</a> function. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="INSTALLLOGMODE_FILESINUSE"></a><a id="installlogmode_filesinuse"></a><dl>
<dt><b>INSTALLLOGMODE_FILESINUSE</b></dt>
</dl>
</td>
<td width="60%">
Files in use information.  When this message is received, a <a href="/windows/desktop/Msi/filesinuse-dialog">FilesInUse Dialog</a> should be displayed. 

</td>
</tr>
<tr>
<td width="40%"><a id="INSTALLLOGMODE_FATALEXIT"></a><a id="installlogmode_fatalexit"></a><dl>
<dt><b>INSTALLLOGMODE_FATALEXIT</b></dt>
</dl>
</td>
<td width="60%">
Premature termination of installation.

</td>
</tr>
<tr>
<td width="40%"><a id="INSTALLLOGMODE_ERROR"></a><a id="installlogmode_error"></a><dl>
<dt><b>INSTALLLOGMODE_ERROR</b></dt>
</dl>
</td>
<td width="60%">
The error messages are logged.

</td>
</tr>
<tr>
<td width="40%"><a id="INSTALLLOGMODE_WARNING"></a><a id="installlogmode_warning"></a><dl>
<dt><b>INSTALLLOGMODE_WARNING</b></dt>
</dl>
</td>
<td width="60%">
The warning messages are logged.

</td>
</tr>
<tr>
<td width="40%"><a id="INSTALLLOGMODE_USER"></a><a id="installlogmode_user"></a><dl>
<dt><b>INSTALLLOGMODE_USER</b></dt>
</dl>
</td>
<td width="60%">
The user requests are logged.

</td>
</tr>
<tr>
<td width="40%"><a id="INSTALLLOGMODE_INFO"></a><a id="installlogmode_info"></a><dl>
<dt><b>INSTALLLOGMODE_INFO</b></dt>
</dl>
</td>
<td width="60%">
The status messages that are not displayed are logged.

</td>
</tr>
<tr>
<td width="40%"><a id="INSTALLLOGMODE_RESOLVESOURCE"></a><a id="installlogmode_resolvesource"></a><dl>
<dt><b>INSTALLLOGMODE_RESOLVESOURCE</b></dt>
</dl>
</td>
<td width="60%">
Request to determine a valid source location.

</td>
</tr>
<tr>
<td width="40%"><a id="INSTALLLOGMODE_RMFILESINUSE"></a><a id="installlogmode_rmfilesinuse"></a><dl>
<dt><b>INSTALLLOGMODE_RMFILESINUSE</b></dt>
</dl>
</td>
<td width="60%">
Files in use information.  When this message is received, a <a href="/windows/desktop/Msi/msirmfilesinuse-dialog">MsiRMFilesInUse Dialog</a> should be displayed. 

</td>
</tr>
<tr>
<td width="40%"><a id="INSTALLLOGMODE_OUTOFDISKSPACE"></a><a id="installlogmode_outofdiskspace"></a><dl>
<dt><b>INSTALLLOGMODE_OUTOFDISKSPACE</b></dt>
</dl>
</td>
<td width="60%">
There was insufficient disk space.

</td>
</tr>
<tr>
<td width="40%"><a id="INSTALLLOGMODE_ACTIONSTART"></a><a id="installlogmode_actionstart"></a><dl>
<dt><b>INSTALLLOGMODE_ACTIONSTART</b></dt>
</dl>
</td>
<td width="60%">
The start of new installation actions are logged.

</td>
</tr>
<tr>
<td width="40%"><a id="INSTALLLOGMODE_ACTIONDATA"></a><a id="installlogmode_actiondata"></a><dl>
<dt><b>INSTALLLOGMODE_ACTIONDATA</b></dt>
</dl>
</td>
<td width="60%">
The data record with the installation action is logged.

</td>
</tr>
<tr>
<td width="40%"><a id="INSTALLLOGMODE_COMMONDATA"></a><a id="installlogmode_commondata"></a><dl>
<dt><b>INSTALLLOGMODE_COMMONDATA</b></dt>
</dl>
</td>
<td width="60%">
The parameters for user-interface initialization are logged.

</td>
</tr>
<tr>
<td width="40%"><a id="INSTALLLOGMODE_PROGRESS"></a><a id="installlogmode_progress"></a><dl>
<dt><b>INSTALLLOGMODE_PROGRESS</b></dt>
</dl>
</td>
<td width="60%">
<a href="/windows/desktop/Msi/p-gly">Progress bar</a> information. This message includes information on units so far and total number of units. For an explanation of the message format, see 
the <a href="/windows/desktop/api/msiquery/nf-msiquery-msiprocessmessage">MsiProcessMessage</a> function. This message is only sent to an external user interface and is not logged.

</td>
</tr>
<tr>
<td width="40%"><a id="INSTALLLOGMODE_INITIALIZE"></a><a id="installlogmode_initialize"></a><dl>
<dt><b>INSTALLLOGMODE_INITIALIZE</b></dt>
</dl>
</td>
<td width="60%">
If this is not a quiet installation, then the <a href="/windows/desktop/Msi/b-gly">basic UI</a> has been initialized. If this is a <a href="/windows/desktop/Msi/f-gly">full UI</a> installation, the <i>full UI</i> is not yet initialized. This message is only sent to an external user interface and is not logged.

</td>
</tr>
<tr>
<td width="40%"><a id="INSTALLLOGMODE_TERMINATE"></a><a id="installlogmode_terminate"></a><dl>
<dt><b>INSTALLLOGMODE_TERMINATE</b></dt>
</dl>
</td>
<td width="60%">
If a <a href="/windows/desktop/Msi/f-gly">full UI</a> is being used, the <i>full UI</i> has ended. If this is not a quiet installation, the <a href="/windows/desktop/Msi/b-gly">basic UI</a> has not yet ended. This message is only sent to an external user interface and is not logged.

</td>
</tr>
<tr>
<td width="40%"><a id="INSTALLLOGMODE_SHOWDIALOG"></a><a id="installlogmode_showdialog"></a><dl>
<dt><b>INSTALLLOGMODE_SHOWDIALOG</b></dt>
</dl>
</td>
<td width="60%">
Sent prior to display of the <a href="/windows/desktop/Msi/f-gly">full UI</a> dialog. This message is only sent to an external user interface and is not logged.

</td>
</tr>
<tr>
<td width="40%"><a id="INSTALLLOGMODE_INSTALLSTART"></a><a id="installlogmode_installstart"></a><dl>
<dt><b>INSTALLLOGMODE_INSTALLSTART</b></dt>
</dl>
</td>
<td width="60%">
Installation of product begins. 

The message contains the product's ProductName and ProductCode.

</td>
</tr>
<tr>
<td width="40%"><a id="INSTALLLOGMODE_INSTALLEND"></a><a id="installlogmode_installend"></a><dl>
<dt><b>INSTALLLOGMODE_INSTALLEND</b></dt>
</dl>
</td>
<td width="60%">
Installation of product ends. 

The message contains the product's ProductName, ProductCode, and return value.

</td>
</tr>
</table>

### -param pvContext [in]

Pointer to an application context that is passed to the callback function. This parameter can be used for error checking.

## -returns

The return value is the previously set external handler, or zero (0) if there was no previously set handler.

## -remarks

To restore the previous UI handler, second call is made to 
<b>MsiSetExternalUI</b> using the 
<a href="/windows/desktop/api/msi/nc-msi-installui_handlera">INSTALLUI_HANDLER</a> returned by the first call to 
<b>MsiSetExternalUI</b> and specifying zero (0) for dwMessageFilter.

The external user interface handler pointed to by the <i>puiHandler</i> parameter does not have full control over the external user interface unless 
<a href="/windows/desktop/api/msi/nf-msi-msisetinternalui">MsiSetInternalUI</a> is called with the <i>dwUILevel</i> parameter set to INSTALLUILEVEL_NONE. If 
<b>MsiSetInternalUI</b> is not called, the internal user interface level defaults to INSTALLUILEVEL_BASIC. As a result, any message not handled by the external user interface handler is handled by Windows Installer. The initial "Preparing to install. . ." dialog always appears even if the external user interface handler handles all messages.

<b>MsiSetExternalUI</b> should only be called from a 
<a href="/windows/desktop/Msi/bootstrapping">Bootstrapping</a> application. You cannot call 
<b>MsiSetExternalUI</b> from a custom action.





> [!NOTE]
> The msi.h header defines MsiSetExternalUI as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/Msi/installer-function-reference">Interface and Logging Functions</a>
