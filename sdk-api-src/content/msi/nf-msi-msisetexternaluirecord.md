---
UID: NF:msi.MsiSetExternalUIRecord
title: MsiSetExternalUIRecord function (msi.h)
description: The MsiSetExternalUIRecord function enables an external user-interface (UI) handler.
helpviewer_keywords: ["INSTALLLOGMODE_ACTIONDATA","INSTALLLOGMODE_ACTIONSTART","INSTALLLOGMODE_COMMONDATA","INSTALLLOGMODE_ERROR","INSTALLLOGMODE_FATALEXIT","INSTALLLOGMODE_FILESINUSE","INSTALLLOGMODE_INFO","INSTALLLOGMODE_INITIALIZE","INSTALLLOGMODE_INSTALLEND","INSTALLLOGMODE_INSTALLSTART","INSTALLLOGMODE_OUTOFDISKSPACE","INSTALLLOGMODE_PROGRESS","INSTALLLOGMODE_RESOLVESOURCE","INSTALLLOGMODE_RMFILESINUSE","INSTALLLOGMODE_SHOWDIALOG","INSTALLLOGMODE_TERMINATE","INSTALLLOGMODE_USER","INSTALLLOGMODE_WARNING","MsiSetExternalUIRecord","MsiSetExternalUIRecord function","msi/MsiSetExternalUIRecord","setup.msisetexternaluirecord"]
old-location: setup\msisetexternaluirecord.htm
tech.root: setup
ms.assetid: f2cd2bb7-0e4f-4d3b-9e6c-6f15661064df
ms.date: 12/05/2018
ms.keywords: INSTALLLOGMODE_ACTIONDATA, INSTALLLOGMODE_ACTIONSTART, INSTALLLOGMODE_COMMONDATA, INSTALLLOGMODE_ERROR, INSTALLLOGMODE_FATALEXIT, INSTALLLOGMODE_FILESINUSE, INSTALLLOGMODE_INFO, INSTALLLOGMODE_INITIALIZE, INSTALLLOGMODE_INSTALLEND, INSTALLLOGMODE_INSTALLSTART, INSTALLLOGMODE_OUTOFDISKSPACE, INSTALLLOGMODE_PROGRESS, INSTALLLOGMODE_RESOLVESOURCE, INSTALLLOGMODE_RMFILESINUSE, INSTALLLOGMODE_SHOWDIALOG, INSTALLLOGMODE_TERMINATE, INSTALLLOGMODE_USER, INSTALLLOGMODE_WARNING, MsiSetExternalUIRecord, MsiSetExternalUIRecord function, msi/MsiSetExternalUIRecord, setup.msisetexternaluirecord
req.header: msi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7. Windows Installer 4.0 or Windows Installer 4.5 on   Windows Server 2008 or Windows Vista. See the Windows Installer Run-Time Requirements for information about the minimum Windows service pack that is required by a Windows Installer version.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: MsiSetExternalUIRecord (ANSI)
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
 - MsiSetExternalUIRecord
 - msi/MsiSetExternalUIRecord
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Msi.dll
 - Ext-MS-Win-MSi-Misc-L1-1-0.dll
api_name:
 - MsiSetExternalUIRecord
 - MsiSetExternalUIRecord
---

# MsiSetExternalUIRecord function


## -description

The <b>MsiSetExternalUIRecord</b> function enables an external user-interface (UI) handler.

## -parameters

### -param puiHandler [in]

Specifies a callback function that conforms to the <a href="/windows/desktop/api/msi/nc-msi-installui_handler_record">INSTALLUI_HANDLER_RECORD</a> specification.

To disable the current external UI handler, call the function with this parameter set to a <b>NULL</b> value.

### -param dwMessageFilter [in]

Specifies which messages to handle using the external message handler. If the external handler returns a non-zero result, then that message is not sent to the UI, instead the message is logged if logging is enabled. For more information, see 
<a href="/windows/desktop/api/msi/nf-msi-msienableloga">MsiEnableLog</a>.

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
Files in use information.

When this message is received, a <a href="/windows/desktop/Msi/filesinuse-dialog">FilesInUse Dialog</a> should be displayed.

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
The is insufficient disk space.

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
The <a href="/windows/desktop/Msi/p-gly">Progress bar</a> information.

This message includes information about units so far and total number of units. This message is only sent to an external user interface and is not logged. For more information, see 
<a href="/windows/desktop/api/msiquery/nf-msiquery-msiprocessmessage">MsiProcessMessage</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="INSTALLLOGMODE_INITIALIZE"></a><a id="installlogmode_initialize"></a><dl>
<dt><b>INSTALLLOGMODE_INITIALIZE</b></dt>
</dl>
</td>
<td width="60%">
If this is not a quiet installation, then the <a href="/windows/desktop/Msi/b-gly">basic UI</a> is initialized.

If this is a full UI installation, the <a href="/windows/desktop/Msi/f-gly">Full UI</a> is not yet initialized.

This message is only sent to an external user interface and is not logged.

</td>
</tr>
<tr>
<td width="40%"><a id="INSTALLLOGMODE_TERMINATE"></a><a id="installlogmode_terminate"></a><dl>
<dt><b>INSTALLLOGMODE_TERMINATE</b></dt>
</dl>
</td>
<td width="60%">
If a full UI is being used, the full UI has ended.

If this is not a quiet installation, the basic UI has not ended.

This message is only sent to an external user interface and is not logged.

</td>
</tr>
<tr>
<td width="40%"><a id="INSTALLLOGMODE_SHOWDIALOG"></a><a id="installlogmode_showdialog"></a><dl>
<dt><b>INSTALLLOGMODE_SHOWDIALOG</b></dt>
</dl>
</td>
<td width="60%">
Sent prior to display of the Full UI dialog.

This message is only sent to an external user interface and is not logged.

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

A pointer to an application context that is passed to the callback function.

This parameter can be used for error checking.

### -param ppuiPrevHandler [out, optional]

Returns the pointer to the previously set callback function that conforms to the <a href="/windows/desktop/api/msi/nc-msi-installui_handler_record">INSTALLUI_HANDLER_RECORD</a> specification, or <b>NULL</b> if no callback is previously set.

## -returns

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SUCCESS</b></dt>
</dl>
</td>
<td width="60%">
The function completes successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_CALL_NOT_IMPLEMENTED</b></dt>
</dl>
</td>
<td width="60%">
This value indicates that an attempt is made to call this function from a custom action.

This function cannot be called from a custom action.

</td>
</tr>
</table>

## -remarks

This function cannot be called from <a href="/windows/desktop/Msi/custom-actions">Custom Actions</a>.

The external UI handler enabled by calling <b>MsiSetExternalUIRecord</b> receives messages in the format of a <a href="/windows/desktop/Msi/record-object">Record Object</a>. The external UI handler enabled by calling <a href="/windows/desktop/api/msi/nf-msi-msisetexternaluia">MsiSetExternalUI</a> receives messages in the format of a string. An external UI is always called before the Windows Installer internal UI. An enabled record-based external UI is called before any string-based external UI. If the record-based external UI handler returns 0 (zero), the message is sent to any enabled string-based external UI handler. If the external UI handler returns a non-zero value, the internal Windows Installer UI handler is suppressed and the messages are considered handled.


This function stores the external user interfaces it has set.  To replace the current external UI handler with a previous handler, call the function and specify the <a href="/windows/desktop/api/msi/nc-msi-installui_handler_record">INSTALLUI_HANDLER_RECORD</a> as the <i>puiHandler</i> parameter and 0 (zero) as the <i>dwMessageFilter</i> parameter.

The external user interface handler pointed to by the <i>puiHandler</i> parameter does not have full control over the external user interface unless 
<a href="/windows/desktop/api/msi/nf-msi-msisetinternalui">MsiSetInternalUI</a> is called with the <i>dwUILevel</i> parameter set to INSTALLUILEVEL_NONE. If 
<b>MsiSetInternalUI</b> is not called, the internal user interface level defaults to INSTALLUILEVEL_BASIC. As a result, any message not handled by the external user interface handler is handled by Windows Installer. The initial "Preparing to install. . ." dialog always appears even if the external user interface handler handles all messages.
    <a href="/windows/desktop/api/msi/nf-msi-msisetexternaluia">MsiSetExternalUI</a> should only be called from an 
<a href="/windows/desktop/Msi/bootstrapping">Bootstrapping</a> application. You cannot call 
<b>MsiSetExternalUI</b> from a custom action.

To disable this external UI handler, call <b>MsiSetExternalUIRecord</b> with a <b>NULL</b> value for the <i>puiHandler</i> parameter.

<b>Windows Installer 2.0 and Windows Installer 3.0:  </b>Not supported. The <b>MsiSetExternalUIRecord</b> function is available beginning with Windows Installer 3.1.

For more information about using a record-based external handler, see <a href="/windows/desktop/Msi/monitoring-an-installation-using-msisetexternaluirecord">Monitoring an Installation Using MsiSetExternalUIRecord</a>.

## -see-also

<a href="/windows/desktop/Msi/installer-function-reference">Interface and Logging Functions</a>



<a href="/windows/desktop/Msi/not-supported-in-windows-installer-version-3-0">Not Supported in Windows Installer 3.0 and earlier</a>