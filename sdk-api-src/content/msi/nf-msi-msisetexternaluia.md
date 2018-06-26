---
UID: NF:msi.MsiSetExternalUIA
title: MsiSetExternalUIA function
author: windows-sdk-content
description: The MsiSetExternalUI function enables an external user-interface handler.
old-location: setup\msisetexternalui.htm
old-project: Msi
ms.assetid: fcbf0607-d048-486f-bec2-f6e9d03e4194
ms.author: windowssdkdev
ms.date: 06/08/2018
ms.keywords: INSTALLLOGMODE_ACTIONDATA, INSTALLLOGMODE_ACTIONSTART, INSTALLLOGMODE_COMMONDATA, INSTALLLOGMODE_ERROR, INSTALLLOGMODE_FATALEXIT, INSTALLLOGMODE_FILESINUSE, INSTALLLOGMODE_INFO, INSTALLLOGMODE_INITIALIZE, INSTALLLOGMODE_INSTALLEND, INSTALLLOGMODE_INSTALLSTART, INSTALLLOGMODE_OUTOFDISKSPACE, INSTALLLOGMODE_PROGRESS, INSTALLLOGMODE_RESOLVESOURCE, INSTALLLOGMODE_RMFILESINUSE, INSTALLLOGMODE_SHOWDIALOG, INSTALLLOGMODE_TERMINATE, INSTALLLOGMODE_USER, INSTALLLOGMODE_WARNING, MsiSetExternalUI, MsiSetExternalUI function, MsiSetExternalUIA, MsiSetExternalUIW, _msi_msisetexternalui, msi/MsiSetExternalUI, msi/MsiSetExternalUIA, msi/MsiSetExternalUIW, setup.msisetexternalui
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
tech.root: 
req.typenames: DRM_LICENSE_ACQ_DATA
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
product: Windows
targetos: Windows
req.lib: Msi.lib
req.dll: Msi.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# MsiSetExternalUIA function


## -description


The 
<b>MsiSetExternalUI</b> function enables an external user-interface handler. This external UI handler is called before the normal internal user-interface handler. The external UI handler has the option to suppress the internal UI by returning a non-zero value to indicate that it has handled the messages. For more information, see 
<a href="https://msdn.microsoft.com/58ef0043-fb30-4f64-9291-e703d7a28bb5">About the User Interface</a>.


## -parameters




### -param puiHandler [in]

Specifies a callback function that conforms to the 
<a href="https://msdn.microsoft.com/76d771d4-12d0-4975-88cc-1921a32a2a09">INSTALLUI_HANDLER</a> specification.


### -param dwMessageFilter [in]

Specifies which messages to handle using the external message handler. If the external handler returns a non-zero result, then that message will not be sent to the UI, instead the message will be logged if logging has been enabled. For more information, see 
the <a href="https://msdn.microsoft.com/117ccd0b-e434-453f-9602-ff50bc85db6e">MsiEnableLog</a> function. 



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
Files in use information.  When this message is received, a <a href="https://msdn.microsoft.com/4246b099-3b70-4983-a68e-eddac801a8c3">FilesInUse Dialog</a> should be displayed. 

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
Files in use information.  When this message is received, a <a href="https://msdn.microsoft.com/e8d93310-388e-4a08-9bce-04c31c33a665">MsiRMFilesInUse Dialog</a> should be displayed. 

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
<a href="p_gly.htm">Progress bar</a> information. This message includes information on units so far and total number of units. For an explanation of the message format, see 
the <a href="https://msdn.microsoft.com/136662bd-b970-4ff3-8ae5-c5e3097ee00d">MsiProcessMessage</a> function. This message is only sent to an external user interface and is not logged.

</td>
</tr>
<tr>
<td width="40%"><a id="INSTALLLOGMODE_INITIALIZE"></a><a id="installlogmode_initialize"></a><dl>
<dt><b>INSTALLLOGMODE_INITIALIZE</b></dt>
</dl>
</td>
<td width="60%">
If this is not a quiet installation, then the <a href="b_gly.htm">basic UI</a> has been initialized. If this is a <a href="f_gly.htm">full UI</a> installation, the <i>full UI</i> is not yet initialized. This message is only sent to an external user interface and is not logged.

</td>
</tr>
<tr>
<td width="40%"><a id="INSTALLLOGMODE_TERMINATE"></a><a id="installlogmode_terminate"></a><dl>
<dt><b>INSTALLLOGMODE_TERMINATE</b></dt>
</dl>
</td>
<td width="60%">
If a <a href="f_gly.htm">full UI</a> is being used, the <i>full UI</i> has ended. If this is not a quiet installation, the <a href="b_gly.htm">basic UI</a> has not yet ended. This message is only sent to an external user interface and is not logged.

</td>
</tr>
<tr>
<td width="40%"><a id="INSTALLLOGMODE_SHOWDIALOG"></a><a id="installlogmode_showdialog"></a><dl>
<dt><b>INSTALLLOGMODE_SHOWDIALOG</b></dt>
</dl>
</td>
<td width="60%">
Sent prior to display of the <a href="f_gly.htm">full UI</a> dialog. This message is only sent to an external user interface and is not logged.

</td>
</tr>
<tr>
<td width="40%"><a id="INSTALLLOGMODE_INSTALLSTART"></a><a id="installlogmode_installstart"></a><dl>
<dt><b><b>INSTALLLOGMODE_INSTALLSTART</b></b></dt>
</dl>
</td>
<td width="60%">
Installation of product begins. 

The message contains the product's ProductName and ProductCode.

</td>
</tr>
<tr>
<td width="40%"><a id="INSTALLLOGMODE_INSTALLEND"></a><a id="installlogmode_installend"></a><dl>
<dt><b><b>INSTALLLOGMODE_INSTALLEND</b></b></dt>
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
<a href="https://msdn.microsoft.com/76d771d4-12d0-4975-88cc-1921a32a2a09">INSTALLUI_HANDLER</a> returned by the first call to 
<b>MsiSetExternalUI</b> and specifying zero (0) for dwMessageFilter.

The external user interface handler pointed to by the <i>puiHandler</i> parameter does not have full control over the external user interface unless 
<a href="https://msdn.microsoft.com/303c2ea9-4c8f-46d3-b587-7c50e2810c28">MsiSetInternalUI</a> is called with the <i>dwUILevel</i> parameter set to INSTALLUILEVEL_NONE. If 
<b>MsiSetInternalUI</b> is not called, the internal user interface level defaults to INSTALLUILEVEL_BASIC. As a result, any message not handled by the external user interface handler is handled by Windows Installer. The initial "Preparing to install. . ." dialog always appears even if the external user interface handler handles all messages.

<b>MsiSetExternalUI</b> should only be called from a 
<a href="https://msdn.microsoft.com/a5174284-2a8c-4510-accf-641fda5be98d">Bootstrapping</a> application. You cannot call 
<b>MsiSetExternalUI</b> from a custom action.




## -see-also




<a href="installer_function_reference.htm">Interface and Logging Functions</a>
 

 

