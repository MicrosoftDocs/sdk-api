---
UID: NF:msiquery.MsiProcessMessage
title: MsiProcessMessage function (msiquery.h)
description: The MsiProcessMessage function sends an error record to the installer for processing.
helpviewer_keywords: ["INSTALLMESSAGE_ACTIONDATA","INSTALLMESSAGE_ACTIONSTART","INSTALLMESSAGE_COMMONDATA","INSTALLMESSAGE_ERROR","INSTALLMESSAGE_FATALEXIT","INSTALLMESSAGE_FILESINUSE","INSTALLMESSAGE_INFO","INSTALLMESSAGE_OUTOFDISKSPACE","INSTALLMESSAGE_PROGRESS","INSTALLMESSAGE_RESOLVESOURCE","INSTALLMESSAGE_RMFILESINUSE","INSTALLMESSAGE_USER","INSTALLMESSAGE_WARNING","MsiProcessMessage","MsiProcessMessage function","_msi_msiprocessmessage","msiquery/MsiProcessMessage","setup.msiprocessmessage"]
old-location: setup\msiprocessmessage.htm
tech.root: setup
ms.assetid: 136662bd-b970-4ff3-8ae5-c5e3097ee00d
ms.date: 12/05/2018
ms.keywords: INSTALLMESSAGE_ACTIONDATA, INSTALLMESSAGE_ACTIONSTART, INSTALLMESSAGE_COMMONDATA, INSTALLMESSAGE_ERROR, INSTALLMESSAGE_FATALEXIT, INSTALLMESSAGE_FILESINUSE, INSTALLMESSAGE_INFO, INSTALLMESSAGE_OUTOFDISKSPACE, INSTALLMESSAGE_PROGRESS, INSTALLMESSAGE_RESOLVESOURCE, INSTALLMESSAGE_RMFILESINUSE, INSTALLMESSAGE_USER, INSTALLMESSAGE_WARNING, MsiProcessMessage, MsiProcessMessage function, _msi_msiprocessmessage, msiquery/MsiProcessMessage, setup.msiprocessmessage
req.header: msiquery.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7. Windows Installer 4.0 or Windows Installer 4.5 on   Windows Server 2008 or Windows Vista. Windows Installer on Windows Server 2003 or Windows XP
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
 - MsiProcessMessage
 - msiquery/MsiProcessMessage
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-msi-misc-l1-1-0.dll
 - Msi.dll
api_name:
 - MsiProcessMessage
---

# MsiProcessMessage function


## -description

The 
<b>MsiProcessMessage</b> function sends an error record to the installer for processing.

## -parameters

### -param hInstall [in]

Handle to the installation provided to a DLL custom action or obtained through <a href="/windows/desktop/api/msi/nf-msi-msiopenpackagea">MsiOpenPackage</a>, <a href="/windows/desktop/api/msi/nf-msi-msiopenpackageexa">MsiOpenPackageEx</a>, or <a href="/windows/desktop/api/msi/nf-msi-msiopenproducta">MsiOpenProduct</a>.

### -param eMessageType [in]

The <i>eMessage</i> parameter must be a value specifying one of the following message types. To display a message box with push buttons or icons, use OR-operators to add INSTALLMESSAGE_ERROR, INSTALLMESSAGE_WARNING, or INSTALLMESSAGE_USER to the standard message box styles used by 
the <a href="/windows/desktop/api/winuser/nf-winuser-messagebox">MessageBox</a> and 
<a href="/windows/desktop/api/winuser/nf-winuser-messageboxexa">MessageBoxEx</a> functions. For more information, see the Remarks below. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="INSTALLMESSAGE_FATALEXIT"></a><a id="installmessage_fatalexit"></a><dl>
<dt><b>INSTALLMESSAGE_FATALEXIT</b></dt>
</dl>
</td>
<td width="60%">
Premature termination, possibly fatal out of memory.

</td>
</tr>
<tr>
<td width="40%"><a id="INSTALLMESSAGE_ERROR"></a><a id="installmessage_error"></a><dl>
<dt><b>INSTALLMESSAGE_ERROR</b></dt>
</dl>
</td>
<td width="60%">
Formatted error message,<div> </div>[1] is message number in 
<a href="/windows/desktop/Msi/error-table">Error table</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="INSTALLMESSAGE_WARNING"></a><a id="installmessage_warning"></a><dl>
<dt><b>INSTALLMESSAGE_WARNING</b></dt>
</dl>
</td>
<td width="60%">
Formatted warning message,<div> </div>[1] is message number in Error table.

</td>
</tr>
<tr>
<td width="40%"><a id="INSTALLMESSAGE_USER"></a><a id="installmessage_user"></a><dl>
<dt><b>INSTALLMESSAGE_USER</b></dt>
</dl>
</td>
<td width="60%">
User request message,<div> </div>[1] is message number in Error table.

</td>
</tr>
<tr>
<td width="40%"><a id="INSTALLMESSAGE_INFO"></a><a id="installmessage_info"></a><dl>
<dt><b>INSTALLMESSAGE_INFO</b></dt>
</dl>
</td>
<td width="60%">
Informative message for log,<div> </div> not to be displayed.

</td>
</tr>
<tr>
<td width="40%"><a id="INSTALLMESSAGE_FILESINUSE"></a><a id="installmessage_filesinuse"></a><dl>
<dt><b>INSTALLMESSAGE_FILESINUSE</b></dt>
</dl>
</td>
<td width="60%">
List of files currently in use that must be closed before being replaced. 

</td>
</tr>
<tr>
<td width="40%"><a id="INSTALLMESSAGE_RESOLVESOURCE"></a><a id="installmessage_resolvesource"></a><dl>
<dt><b>INSTALLMESSAGE_RESOLVESOURCE</b></dt>
</dl>
</td>
<td width="60%">
Request to determine a valid source location.

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
Insufficient disk space message.

</td>
</tr>
<tr>
<td width="40%"><a id="INSTALLMESSAGE_ACTIONSTART"></a><a id="installmessage_actionstart"></a><dl>
<dt><b>INSTALLMESSAGE_ACTIONSTART</b></dt>
</dl>
</td>
<td width="60%">
Progress: start of action,<div> </div>[1] action name,<div> </div>[2] description,<div> </div>[3] template for ACTIONDATA messages.

</td>
</tr>
<tr>
<td width="40%"><a id="INSTALLMESSAGE_ACTIONDATA"></a><a id="installmessage_actiondata"></a><dl>
<dt><b>INSTALLMESSAGE_ACTIONDATA</b></dt>
</dl>
</td>
<td width="60%">
Action data. Record fields correspond to the template of ACTIONSTART message.

</td>
</tr>
<tr>
<td width="40%"><a id="INSTALLMESSAGE_PROGRESS"></a><a id="installmessage_progress"></a><dl>
<dt><b>INSTALLMESSAGE_PROGRESS</b></dt>
</dl>
</td>
<td width="60%">
Progress bar information. See the description of record fields below.

</td>
</tr>
<tr>
<td width="40%"><a id="INSTALLMESSAGE_COMMONDATA"></a><a id="installmessage_commondata"></a><dl>
<dt><b>INSTALLMESSAGE_COMMONDATA</b></dt>
</dl>
</td>
<td width="60%">
To enable the Cancel button set [1] to 2 and [2] to 1. 




To disable the Cancel button set [1] to 2 and [2] to 0

</td>
</tr>
</table>

### -param hRecord [in]

Handle to a record containing message format and data.

## -returns

This function returns int.

## -remarks

The 
<b>MsiProcessMessage</b> function performs any enabled logging operations and defers execution. You can selectively enable logging for various message types.

For INSTALLMESSAGE_FATALEXIT, INSTALLMESSAGE_ERROR, INSTALLMESSAGE_WARNING, and INSTALLMESSAGE_USER messages, if field 0 is not set field 1 must be set to the error code corresponding to the error message in the 
<a href="/windows/desktop/Msi/error-table">Error table</a>. Then, the message is formatted using the template from the Error table before passing it to the user-interface handler for display.

<h3><a id="Record_Fields_for_Progress_Bar_Messages"></a><a id="record_fields_for_progress_bar_messages"></a><a id="RECORD_FIELDS_FOR_PROGRESS_BAR_MESSAGES"></a>Record Fields for Progress Bar Messages</h3>
The following describes the record fields when eMessageType is set to INSTALLMESSAGE_PROGRESS. Field 1 specifies the type of the progress message. The meaning of the other fields depend upon the value in this field. The possible values that can be set into Field 1 are as follows.

<table>
<tr>
<th>Field 1 value</th>
<th>Field 1 description</th>
</tr>
<tr>
<td>0</td>
<td>Resets progress bar and sets the expected total number of ticks in the bar.</td>
</tr>
<tr>
<td>1</td>
<td>Provides information related to progress messages to be sent by the current action.</td>
</tr>
<tr>
<td>2</td>
<td>Increments the progress bar.</td>
</tr>
<tr>
<td>3</td>
<td>Enables an action (such as CustomAction) to add ticks to the expected total number of progress of the progress bar.</td>
</tr>
</table>
 

The meaning of Field 2 depends upon the value in Field 1 as follows.

<table>
<tr>
<th>Field 1 value</th>
<th>Field 2 description</th>
</tr>
<tr>
<td>0</td>
<td>Expected total number of ticks in the progress bar.</td>
</tr>
<tr>
<td>1</td>
<td>Number of ticks the progress bar moves for each ActionData message that is sent by the current action. This field is ignored if Field 3 is 0.</td>
</tr>
<tr>
<td>2</td>
<td>Number of ticks the progress bar has moved.</td>
</tr>
<tr>
<td>3</td>
<td>Number of ticks to add to total expected progress.</td>
</tr>
</table>
 

The meaning of Field 3 depends upon the value in Field 1 as follows.

<table>
<tr>
<th>Field 1 value</th>
<th>Field 3 value</th>
<th>Field 3 description</th>
</tr>
<tr>
<td>0</td>
<td>0</td>
<td>Forward progress bar (left to right)</td>
</tr>
<tr>
<td> </td>
<td>1</td>
<td>Backward progress bar (right to left)</td>
</tr>
<tr>
<td>1</td>
<td>0</td>
<td>The current action will send explicit ProgressReport messages.</td>
</tr>
<tr>
<td> </td>
<td>1</td>
<td>Increment the progress bar by the number of ticks specified in Field 2 each time an ActionData message is sent by the current action.</td>
</tr>
<tr>
<td>2</td>
<td>Unused</td>
<td> </td>
</tr>
<tr>
<td>3</td>
<td>Unused</td>
<td> </td>
</tr>
</table>
 

The meaning of Field 4 depends upon the value in Field 1 as follows.

<table>
<tr>
<th>Field 1 value</th>
<th>Field 4 value</th>
<th>Field 4 description</th>
</tr>
<tr>
<td>0</td>
<td>0</td>
<td>Execution is in progress. In this case, the UI could calculate and display the time remaining.</td>
</tr>
<tr>
<td> </td>
<td>1</td>
<td>Creating the execution script. In this case, the UI could display a message to please wait while the installer finishes preparing the installation.</td>
</tr>
<tr>
<td>1</td>
<td>Unused</td>
<td> </td>
</tr>
<tr>
<td>2</td>
<td>Unused</td>
<td> </td>
</tr>
<tr>
<td>3</td>
<td>Unused</td>
<td> </td>
</tr>
</table>
 

For more information and a code sample, see 
<a href="/windows/desktop/Msi/adding-custom-actions-to-the-progressbar">Adding Custom Actions to the ProgressBar</a>.

<h3><a id="Display_of_Message_Boxes"></a><a id="display_of_message_boxes"></a><a id="DISPLAY_OF_MESSAGE_BOXES"></a>Display of Message Boxes</h3>
To display a message box with push buttons or icons, use OR-operators to add INSTALLMESSAGE_ERROR, INSTALLMESSAGE_WARNING, or INSTALLMESSAGE_USER with the message box options used by <a href="/windows/desktop/api/winuser/nf-winuser-messagebox">MessageBox</a> and <a href="/windows/desktop/api/winuser/nf-winuser-messageboxexa">MessageBoxEx</a>. The available push button options are MB_OK, MB_OKCANCEL, MB_ABORTRETRYIGNORE, MB_YESNOCANCEL, MB_YESNO, and MB_RETRYCANCEL. The available default button options are MB_DEFBUTTON1, MB_DEFBUTTON2, and MB_DEFBUTTON3. The available icon options are MB_ICONERROR, MB_ICONQUESTION, MB_ICONWARNING, and MB_ICONINFORMATION. If no icon options is specified, Windows Installer chooses a default icon style based upon the message type.

For example, the following call to 
<b>MsiProcessMessage</b> sends an INSTALLMESSAGE_ERROR message with the MB_ICONWARNING icon and the MB_ABORTRETRYCANCEL buttons.


```cpp
PMSIHANDLE hInstall;
PMSIHANDLE hRec;
MsiProcessMessage(hInstall, 
                  INSTALLMESSAGE(INSTALLMESSAGE_ERROR|MB_ABORTRETRYIGNORE|MB_ICONWARNING),
                  hRec);

```


If a custom action calls <b>MsiProcessMessage</b>, the custom action should be capable of handling a cancellation by the user and should return ERROR_INSTALL_USEREXIT.


For more information on sending messages with 
<b>MsiProcessMessage</b>, see the 
<a href="/windows/desktop/Msi/sending-messages-to-windows-installer-using-msiprocessmessage">Sending Messages to Windows Installer Using MsiProcessMessage</a>.

## -see-also

<a href="/windows/desktop/Msi/database-functions">Installer Action Functions</a>



<a href="/windows/desktop/Msi/sending-messages-to-windows-installer-using-msiprocessmessage">Sending Messages to Windows Installer Using MsiProcessMessage</a>