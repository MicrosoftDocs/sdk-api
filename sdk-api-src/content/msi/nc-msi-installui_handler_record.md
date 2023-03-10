---
UID: NC:msi.INSTALLUI_HANDLER_RECORD
title: INSTALLUI_HANDLER_RECORD (msi.h)
description: The INSTALLUI_HANDLER_RECORD function prototype defines a callback function that the installer calls for progress notification and error messages. Call the MsiSetExternalUIRecord function to enable a record-base external user-interface (UI) handler.
helpviewer_keywords: ["INSTALLMESSAGE_ACTIONDATA","INSTALLMESSAGE_ACTIONSTART","INSTALLMESSAGE_COMMONDATA","INSTALLMESSAGE_ERROR","INSTALLMESSAGE_FATALEXIT","INSTALLMESSAGE_FILESINUSE","INSTALLMESSAGE_INFO","INSTALLMESSAGE_INITIALIZE","INSTALLMESSAGE_INSTALLEND","INSTALLMESSAGE_INSTALLSTART","INSTALLMESSAGE_OUTOFDISKSPACE","INSTALLMESSAGE_PROGRESS","INSTALLMESSAGE_RESOLVESOURCE","INSTALLMESSAGE_RMFILESINUSE","INSTALLMESSAGE_SHOWDIALOG","INSTALLMESSAGE_TERMINATE","INSTALLMESSAGE_USER","INSTALLMESSAGE_WARNING","INSTALLUI_HANDLER","INSTALLUI_HANDLER callback function pointer","INSTALLUI_HANDLER_RECORD","INSTALLUI_HANDLER_RECORD callback","INSTALLUI_HANDLER_RECORD callback function","InstallUIHandlerRecord","MB_ABORTRETRYIGNORE","MB_DEFBUTTON1","MB_DEFBUTTON2","MB_DEFBUTTON3","MB_ICONEXCLAMATION","MB_ICONWARNING","MB_ICONINFORMATION","MB_ICONASTERISK","MB_ICONQUESTION","MB_ICONSTOP","MB_ICONERROR","MB_ICONHAND","MB_OK","MB_OKCANCEL","MB_RETRYCANCEL","MB_YESNO","MB_YESNOCANCEL","msi/INSTALLUI_HANDLER_RECORD","setup.installui_handler_record"]
old-location: setup\installui_handler_record.htm
tech.root: setup
ms.assetid: de714639-f519-4c78-811e-b3b1f04d8450
ms.date: 12/05/2018
ms.keywords: INSTALLMESSAGE_ACTIONDATA, INSTALLMESSAGE_ACTIONSTART, INSTALLMESSAGE_COMMONDATA, INSTALLMESSAGE_ERROR, INSTALLMESSAGE_FATALEXIT, INSTALLMESSAGE_FILESINUSE, INSTALLMESSAGE_INFO, INSTALLMESSAGE_INITIALIZE, INSTALLMESSAGE_INSTALLEND, INSTALLMESSAGE_INSTALLSTART, INSTALLMESSAGE_OUTOFDISKSPACE, INSTALLMESSAGE_PROGRESS, INSTALLMESSAGE_RESOLVESOURCE, INSTALLMESSAGE_RMFILESINUSE, INSTALLMESSAGE_SHOWDIALOG, INSTALLMESSAGE_TERMINATE, INSTALLMESSAGE_USER, INSTALLMESSAGE_WARNING, INSTALLUI_HANDLER, INSTALLUI_HANDLER callback function pointer, INSTALLUI_HANDLER_RECORD, INSTALLUI_HANDLER_RECORD callback, INSTALLUI_HANDLER_RECORD callback function, InstallUIHandlerRecord, MB_ABORTRETRYIGNORE, MB_DEFBUTTON1, MB_DEFBUTTON2, MB_DEFBUTTON3, MB_ICONEXCLAMATION,MB_ICONWARNING, MB_ICONINFORMATION,MB_ICONASTERISK, MB_ICONQUESTION, MB_ICONSTOP,MB_ICONERROR,MB_ICONHAND, MB_OK, MB_OKCANCEL, MB_RETRYCANCEL, MB_YESNO, MB_YESNOCANCEL, msi/INSTALLUI_HANDLER_RECORD, setup.installui_handler_record
req.header: msi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7. Windows Installer 4.0 or Windows Installer 4.5 on   Windows Server 2008 or Windows Vista. Windows Installer 3.1 on Windows Server 2003 or Windows XP.
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - INSTALLUI_HANDLER_RECORD
 - msi/INSTALLUI_HANDLER_RECORD
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Msi.h
api_name:
 - INSTALLUI_HANDLER
---

# INSTALLUI_HANDLER_RECORD callback function


## -description

The <b>INSTALLUI_HANDLER_RECORD</b> function 
    prototype defines a callback function that the installer calls for progress notification and error messages. Call 
    the <b>MsiSetExternalUIRecord</b> function to enable a record-base external 
    user-interface (UI) handler.


<b>Windows Installer 3.0 and Windows Installer 2.0:  </b>Not supported. Available beginning with Windows Installer version 3.1 and later.

## -parameters

### -param pvContext

Pointer to an application context passed to the 
      <a href="/windows/desktop/api/msi/nf-msi-msisetexternaluirecord">MsiSetExternalUIRecord</a> function. This parameter 
      can be used for error checking.

### -param iMessageType

Specifies a combination of one message box style, one message box icon type, one default button, and one 
      installation message type. This parameter must be one of the following.

<table>
<tr>
<th>Message box StylesFlag</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MB_ABORTRETRYIGNORE"></a><a id="mb_abortretryignore"></a><dl>
<dt><b>MB_ABORTRETRYIGNORE</b></dt>
</dl>
</td>
<td width="60%">
The message box contains the <b>Abort</b>, <b>Retry</b>, and <b>Ignore</b> buttons.

</td>
</tr>
<tr>
<td width="40%"><a id="MB_OK"></a><a id="mb_ok"></a><dl>
<dt><b>MB_OK</b></dt>
</dl>
</td>
<td width="60%">
The message box contains the <b>OK</b> button. This is the default.

</td>
</tr>
<tr>
<td width="40%"><a id="MB_OKCANCEL"></a><a id="mb_okcancel"></a><dl>
<dt><b>MB_OKCANCEL</b></dt>
</dl>
</td>
<td width="60%">
The message box contains the <b>OK</b> and <b>Cancel</b> buttons.

</td>
</tr>
<tr>
<td width="40%"><a id="MB_RETRYCANCEL"></a><a id="mb_retrycancel"></a><dl>
<dt><b>MB_RETRYCANCEL</b></dt>
</dl>
</td>
<td width="60%">
The message box contains the <b>Retry</b> and <b>Cancel</b> buttons.

</td>
</tr>
<tr>
<td width="40%"><a id="MB_YESNO"></a><a id="mb_yesno"></a><dl>
<dt><b>MB_YESNO</b></dt>
</dl>
</td>
<td width="60%">
The message box contains the <b>Yes</b> and <b>No</b> buttons.

</td>
</tr>
<tr>
<td width="40%"><a id="MB_YESNOCANCEL"></a><a id="mb_yesnocancel"></a><dl>
<dt><b>MB_YESNOCANCEL</b></dt>
</dl>
</td>
<td width="60%">
The message box contains the <b>Yes</b>, <b>No</b>, and <b>Cancel</b> buttons.

</td>
</tr>
</table>
 

<table>
<tr>
<th>Message box IconTypesFlag</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MB_ICONEXCLAMATION__MB_ICONWARNING"></a><a id="mb_iconexclamation__mb_iconwarning"></a><dl>
<dt><b>MB_ICONEXCLAMATION, MB_ICONWARNING</b></dt>
</dl>
</td>
<td width="60%">
An exclamation point appears in the message box.

</td>
</tr>
<tr>
<td width="40%"><a id="MB_ICONINFORMATION__MB_ICONASTERISK"></a><a id="mb_iconinformation__mb_iconasterisk"></a><dl>
<dt><b>MB_ICONINFORMATION, MB_ICONASTERISK</b></dt>
</dl>
</td>
<td width="60%">
The information sign appears in the message box.

</td>
</tr>
<tr>
<td width="40%"><a id="MB_ICONQUESTION"></a><a id="mb_iconquestion"></a><dl>
<dt><b>MB_ICONQUESTION</b></dt>
</dl>
</td>
<td width="60%">
A question mark appears in the message box.

</td>
</tr>
<tr>
<td width="40%"><a id="MB_ICONSTOP__MB_ICONERROR__MB_ICONHAND"></a><a id="mb_iconstop__mb_iconerror__mb_iconhand"></a><dl>
<dt><b>MB_ICONSTOP, MB_ICONERROR, MB_ICONHAND</b></dt>
</dl>
</td>
<td width="60%">
A stop sign appears in the message box.

</td>
</tr>
</table>
 

<table>
<tr>
<th>Default ButtonsFlag</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MB_DEFBUTTON1"></a><a id="mb_defbutton1"></a><dl>
<dt><b>MB_DEFBUTTON1</b></dt>
</dl>
</td>
<td width="60%">
The first button is the default button.

</td>
</tr>
<tr>
<td width="40%"><a id="MB_DEFBUTTON2"></a><a id="mb_defbutton2"></a><dl>
<dt><b>MB_DEFBUTTON2</b></dt>
</dl>
</td>
<td width="60%">
The second button is the default button.

</td>
</tr>
<tr>
<td width="40%"><a id="MB_DEFBUTTON3"></a><a id="mb_defbutton3"></a><dl>
<dt><b>MB_DEFBUTTON3</b></dt>
</dl>
</td>
<td width="60%">
The third button is the default button.

</td>
</tr>
</table>
 

<table>
<tr>
<th>Install message TypesFlag</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="INSTALLMESSAGE_FATALEXIT"></a><a id="installmessage_fatalexit"></a><dl>
<dt><b>INSTALLMESSAGE_FATALEXIT</b></dt>
</dl>
</td>
<td width="60%">
Premature termination

</td>
</tr>
<tr>
<td width="40%"><a id="INSTALLMESSAGE_ERROR"></a><a id="installmessage_error"></a><dl>
<dt><b>INSTALLMESSAGE_ERROR</b></dt>
</dl>
</td>
<td width="60%">
Formatted error message

</td>
</tr>
<tr>
<td width="40%"><a id="INSTALLMESSAGE_WARNING"></a><a id="installmessage_warning"></a><dl>
<dt><b>INSTALLMESSAGE_WARNING</b></dt>
</dl>
</td>
<td width="60%">
Formatted warning message

</td>
</tr>
<tr>
<td width="40%"><a id="INSTALLMESSAGE_USER"></a><a id="installmessage_user"></a><dl>
<dt><b>INSTALLMESSAGE_USER</b></dt>
</dl>
</td>
<td width="60%">
User request message.

</td>
</tr>
<tr>
<td width="40%"><a id="INSTALLMESSAGE_INFO"></a><a id="installmessage_info"></a><dl>
<dt><b>INSTALLMESSAGE_INFO</b></dt>
</dl>
</td>
<td width="60%">
Informative message for log

</td>
</tr>
<tr>
<td width="40%"><a id="INSTALLMESSAGE_FILESINUSE"></a><a id="installmessage_filesinuse"></a><dl>
<dt><b>INSTALLMESSAGE_FILESINUSE</b></dt>
</dl>
</td>
<td width="60%">
List of files currently in use that must be closed before being replaced

</td>
</tr>
<tr>
<td width="40%"><a id="INSTALLMESSAGE_RESOLVESOURCE"></a><a id="installmessage_resolvesource"></a><dl>
<dt><b>INSTALLMESSAGE_RESOLVESOURCE</b></dt>
</dl>
</td>
<td width="60%">
Request to determine a valid source location

</td>
</tr>
<tr>
<td width="40%"><a id="INSTALLMESSAGE_RMFILESINUSE"></a><a id="installmessage_rmfilesinuse"></a><dl>
<dt><b>INSTALLMESSAGE_RMFILESINUSE</b></dt>
</dl>
</td>
<td width="60%">
List of files currently in use that must be closed before being replaced. Available beginning with Windows Installer version 4.0. For more information about this message see <a href="/windows/desktop/Msi/using-restart-manager-with-an-external-ui-">Using Restart Manager with an External UI</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="INSTALLMESSAGE_OUTOFDISKSPACE"></a><a id="installmessage_outofdiskspace"></a><dl>
<dt><b>INSTALLMESSAGE_OUTOFDISKSPACE</b></dt>
</dl>
</td>
<td width="60%">
Insufficient disk space message

</td>
</tr>
<tr>
<td width="40%"><a id="INSTALLMESSAGE_ACTIONSTART"></a><a id="installmessage_actionstart"></a><dl>
<dt><b>INSTALLMESSAGE_ACTIONSTART</b></dt>
</dl>
</td>
<td width="60%">
Start of action message. This message includes the action name and description.

</td>
</tr>
<tr>
<td width="40%"><a id="INSTALLMESSAGE_ACTIONDATA"></a><a id="installmessage_actiondata"></a><dl>
<dt><b>INSTALLMESSAGE_ACTIONDATA</b></dt>
</dl>
</td>
<td width="60%">
Formatted data associated with the individual action item.

</td>
</tr>
<tr>
<td width="40%"><a id="INSTALLMESSAGE_PROGRESS"></a><a id="installmessage_progress"></a><dl>
<dt><b>INSTALLMESSAGE_PROGRESS</b></dt>
</dl>
</td>
<td width="60%">
Progress gauge information. This message includes information on units so far and total number of units.

</td>
</tr>
<tr>
<td width="40%"><a id="INSTALLMESSAGE_COMMONDATA"></a><a id="installmessage_commondata"></a><dl>
<dt><b>INSTALLMESSAGE_COMMONDATA</b></dt>
</dl>
</td>
<td width="60%">
Formatted dialog information for user interface.

</td>
</tr>
<tr>
<td width="40%"><a id="INSTALLMESSAGE_INITIALIZE"></a><a id="installmessage_initialize"></a><dl>
<dt><b>INSTALLMESSAGE_INITIALIZE</b></dt>
</dl>
</td>
<td width="60%">
Sent prior to UI initialization, no string data

</td>
</tr>
<tr>
<td width="40%"><a id="INSTALLMESSAGE_TERMINATE"></a><a id="installmessage_terminate"></a><dl>
<dt><b>INSTALLMESSAGE_TERMINATE</b></dt>
</dl>
</td>
<td width="60%">
Sent after UI termination, no string data

</td>
</tr>
<tr>
<td width="40%"><a id="INSTALLMESSAGE_SHOWDIALOG"></a><a id="installmessage_showdialog"></a><dl>
<dt><b>INSTALLMESSAGE_SHOWDIALOG</b></dt>
</dl>
</td>
<td width="60%">
Sent prior to display of authored dialog or wizard

</td>
</tr>
<tr>
<td width="40%"><a id="INSTALLMESSAGE_INSTALLSTART"></a><a id="installmessage_installstart"></a><dl>
<dt><b>INSTALLMESSAGE_INSTALLSTART</b></dt>
</dl>
</td>
<td width="60%">
Sent prior to installation of product.

</td>
</tr>
<tr>
<td width="40%"><a id="INSTALLMESSAGE_INSTALLEND"></a><a id="installmessage_installend"></a><dl>
<dt><b>INSTALLMESSAGE_INSTALLEND</b></dt>
</dl>
</td>
<td width="60%">
Sent after installation of product.

</td>
</tr>
</table>
 


<div> </div>


The following defaults should be used if any of the preceding messages are missing: MB_OK, no icon, and 
       MB_DEFBUTTON1. There is no default installation message type; a message type is always specified.

### -param hRecord

Specifies a handle to the record object. For information about record objects, see the <a href="/windows/win32/msi/database-functions#record-processing-functions">Record Processing Functions</a>.

## -returns

The following return values map to the buttons specified by the message box style:

IDOK<div> </div>IDCANCEL<div> </div>IDABORT<div> </div>IDRETRY<div> </div>IDIGNORE<div> </div>IDYES<div> </div>IDNO

## -remarks

This type of external UI handler should be used when it is known what type of errors or messages the caller is 
    interested in, and wants to avoid the overhead of parsing the string message that is sent to an external UI 
    handler of INSTALLUI_HANDLER type, but retrieve the data of interest from fields of hRecord.

For more information on returning values from an external user interface handler, see the 
    <a href="/windows/desktop/Msi/returning-values-from-an-external-user-interface-handler">Returning Values from an 
    External User Interface Handler</a> topic. The hRecord object sent to the record-based external UI handler is 
    owned by Windows Installer and is valid only for the callback's lifetime.  The callback should extract from the 
    record any data it needs and it should not close that handle.

Any attempt by a record-based external UI handler to alter the data in the hRecord object will be ignored by 
    Windows Installer.

For more information about using a record-based external handler, see <a href="/windows/desktop/Msi/monitoring-an-installation-using-msisetexternaluirecord">Monitoring an Installation Using MsiSetExternalUIRecord</a>.

## -see-also

<a href="/windows/desktop/api/msi/nf-msi-msisetexternaluia">MsiSetExternalUI</a>



<a href="/windows/desktop/Msi/not-supported-in-windows-installer-version-3-0">Not Supported in Windows Installer 3.0 and earlier</a>