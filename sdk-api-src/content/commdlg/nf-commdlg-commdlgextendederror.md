---
UID: NF:commdlg.CommDlgExtendedError
title: CommDlgExtendedError function (commdlg.h)
description: The CommDlgExtendedError function (commdlg.h) returns a common dialog box error code. 
helpviewer_keywords: ["CommDlgExtendedError","CommDlgExtendedError function [Dialog Boxes]","_win32_CommDlgExtendedError","_win32_commdlgextendederror_cpp","commdlg/CommDlgExtendedError","dlgbox.commdlgextendederror","winui._win32_commdlgextendederror"]
old-location: dlgbox\commdlgextendederror.htm
tech.root: dlgbox
ms.assetid: VS|winui|~\winui\windowsuserinterface\userinput\commondialogboxlibrary\commondialogboxreference\commondialogboxfunctions\commdlgextendederror.htm
ms.date: 08/16/2022
ms.keywords: CommDlgExtendedError, CommDlgExtendedError function [Dialog Boxes], _win32_CommDlgExtendedError, _win32_commdlgextendederror_cpp, commdlg/CommDlgExtendedError, dlgbox.commdlgextendederror, winui._win32_commdlgextendederror
req.header: commdlg.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Comdlg32.lib
req.dll: Comdlg32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - commdlg/CommDlgExtendedError
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Comdlg32.dll
 - ext-ms-win-shell-comdlg32-l1-1-0.dll
 - ext-ms-win-shell-comdlg32-l1-1-1.dll
api_name:
 - CommDlgExtendedError
req.apiset: ext-ms-win-shell-comdlg32-l1-1-0 (introduced in Windows 10, version 10.0.10240)
---

# CommDlgExtendedError function

## -description

Returns a common dialog box error code. This code indicates the most recent error to occur during the execution of one of the common dialog box functions.

## -returns

Type: <b>DWORD</b>

If the most recent call to a common dialog box function succeeded, the return value is undefined. If the common dialog box function returned <b>FALSE</b> because the user closed or canceled the dialog box, the return value is zero. Otherwise, the return value is a nonzero error code.

The <b>CommDlgExtendedError</b> function can return general error codes for any of the common dialog box functions. In addition, there are error codes that are returned only for a specific common dialog box. All of these error codes are defined in Cderr.h. The following general error codes can be returned for any of the common dialog box functions.

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CDERR_DIALOGFAILURE</b></dt>
<dt>0xFFFF</dt>
</dl>
</td>
<td width="60%">
The dialog box could not be created. The common dialog box function's call to the <a href="/windows/desktop/api/winuser/nf-winuser-dialogboxa">DialogBox</a> function failed. For example, this error occurs if the common dialog box call specifies an invalid window handle.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CDERR_FINDRESFAILURE</b></dt>
<dt>0x0006</dt>
</dl>
</td>
<td width="60%">
The common dialog box function failed to find a specified resource.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CDERR_INITIALIZATION</b></dt>
<dt>0x0002</dt>
</dl>
</td>
<td width="60%">
The common dialog box function failed during initialization. This error often occurs when sufficient memory is not available.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CDERR_LOADRESFAILURE</b></dt>
<dt>0x0007</dt>
</dl>
</td>
<td width="60%">
The common dialog box function failed to load a specified resource.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CDERR_LOADSTRFAILURE</b></dt>
<dt>0x0005</dt>
</dl>
</td>
<td width="60%">
The common dialog box function failed to load a specified string.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CDERR_LOCKRESFAILURE</b></dt>
<dt>0x0008</dt>
</dl>
</td>
<td width="60%">
The common dialog box function failed to lock a specified resource.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CDERR_MEMALLOCFAILURE</b></dt>
<dt>0x0009</dt>
</dl>
</td>
<td width="60%">
The common dialog box function was unable to allocate memory for internal structures.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CDERR_MEMLOCKFAILURE</b></dt>
<dt>0x000A</dt>
</dl>
</td>
<td width="60%">
The common dialog box function was unable to lock the memory associated with a handle.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CDERR_NOHINSTANCE</b></dt>
<dt>0x0004</dt>
</dl>
</td>
<td width="60%">
The <b>ENABLETEMPLATE</b> flag was set in the <b>Flags</b> member of the initialization structure for the corresponding common dialog box, but you failed to provide a corresponding instance handle.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CDERR_NOHOOK</b></dt>
<dt>0x000B</dt>
</dl>
</td>
<td width="60%">
The <b>ENABLEHOOK</b> flag was set in the <b>Flags</b> member of the initialization structure for the corresponding common dialog box, but you failed to provide a pointer to a corresponding hook procedure.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CDERR_NOTEMPLATE</b></dt>
<dt>0x0003</dt>
</dl>
</td>
<td width="60%">
The <b>ENABLETEMPLATE</b> flag was set in the <b>Flags</b> member of the initialization structure for the corresponding common dialog box, but you failed to provide a corresponding template.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CDERR_REGISTERMSGFAIL</b></dt>
<dt>0x000C</dt>
</dl>
</td>
<td width="60%">
The <a href="/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea">RegisterWindowMessage</a> function returned an error code when it was called by the common dialog box function.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CDERR_STRUCTSIZE</b></dt>
<dt>0x0001</dt>
</dl>
</td>
<td width="60%">
The <b>lStructSize</b> member of the initialization structure for the corresponding common dialog box is invalid.

</td>
</tr>
</table>
 

The following error codes can be returned for the <a href="/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)">PrintDlg</a> function.

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PDERR_CREATEICFAILURE</b></dt>
<dt>0x100A</dt>
</dl>
</td>
<td width="60%">
The <a href="/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)">PrintDlg</a> function failed when it attempted to create an information context.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PDERR_DEFAULTDIFFERENT</b></dt>
<dt>0x100C</dt>
</dl>
</td>
<td width="60%">
You called the <a href="/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)">PrintDlg</a> function with the <b>DN_DEFAULTPRN</b> flag specified in the <b>wDefault</b> member of the <a href="/windows/desktop/api/commdlg/ns-commdlg-devnames">DEVNAMES</a> structure, but the printer described by the other structure members did not match the current default printer. This error occurs when you store the <b>DEVNAMES</b> structure, and the user changes the default printer by using the Control Panel.

To use the printer described by the <a href="/windows/desktop/api/commdlg/ns-commdlg-devnames">DEVNAMES</a> structure, clear the <b>DN_DEFAULTPRN</b> flag and call <a href="/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)">PrintDlg</a> again.

To use the default printer, replace the <a href="/windows/desktop/api/commdlg/ns-commdlg-devnames">DEVNAMES</a> structure (and the  structure, if one exists) with <b>NULL</b>; and call <a href="/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)">PrintDlg</a> again.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PDERR_DNDMMISMATCH</b></dt>
<dt>0x1009</dt>
</dl>
</td>
<td width="60%">
The data in the <a href="/windows/win32/api/wingdi/ns-wingdi-devmodea">DEVMODE</a> and <a href="/windows/desktop/api/commdlg/ns-commdlg-devnames">DEVNAMES</a> structures describes two different printers.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PDERR_GETDEVMODEFAIL</b></dt>
<dt>0x1005</dt>
</dl>
</td>
<td width="60%">
The printer driver failed to initialize a <a href="/windows/win32/api/wingdi/ns-wingdi-devmodea">DEVMODE</a> structure.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PDERR_INITFAILURE</b></dt>
<dt>0x1006</dt>
</dl>
</td>
<td width="60%">
The <a href="/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)">PrintDlg</a> function failed during initialization, and there is no more specific extended error code to describe the failure. This is the generic default error code for the function.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PDERR_LOADDRVFAILURE</b></dt>
<dt>0x1004</dt>
</dl>
</td>
<td width="60%">
The <a href="/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)">PrintDlg</a> function failed to load the device driver for the specified printer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PDERR_NODEFAULTPRN</b></dt>
<dt>0x1008</dt>
</dl>
</td>
<td width="60%">
A default printer does not exist.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PDERR_NODEVICES</b></dt>
<dt>0x1007</dt>
</dl>
</td>
<td width="60%">
No printer drivers were found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PDERR_PARSEFAILURE</b></dt>
<dt>0x1002</dt>
</dl>
</td>
<td width="60%">
The <a href="/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)">PrintDlg</a> function failed to parse the strings in the [devices] section of the WIN.INI file.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PDERR_PRINTERNOTFOUND</b></dt>
<dt>0x100B</dt>
</dl>
</td>
<td width="60%">
The [devices] section of the WIN.INI file did not contain an entry for the requested printer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PDERR_RETDEFFAILURE</b></dt>
<dt>0x1003</dt>
</dl>
</td>
<td width="60%">
The PD_RETURNDEFAULT flag was specified in the <b>Flags</b> member of the <a href="/windows/win32/api/commdlg/ns-commdlg-printdlga">PRINTDLG</a> structure, but the 
							<b>hDevMode</b> or <b>hDevNames</b> member was not <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PDERR_SETUPFAILURE</b></dt>
<dt>0x1001</dt>
</dl>
</td>
<td width="60%">
The <a href="/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)">PrintDlg</a> function failed to load the required resources.

</td>
</tr>
</table>
 

The following error codes can be returned for the <a href="/previous-versions/windows/desktop/legacy/ms646914(v=vs.85)">ChooseFont</a> function.

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CFERR_MAXLESSTHANMIN</b></dt>
<dt>0x2002</dt>
</dl>
</td>
<td width="60%">
The size specified in the <b>nSizeMax</b> member of the <a href="/windows/desktop/api/commdlg/ns-commdlg-choosefonta">CHOOSEFONT</a> structure is less than the size specified in the 
							<b>nSizeMin</b> member.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CFERR_NOFONTS</b></dt>
<dt>0x2001</dt>
</dl>
</td>
<td width="60%">
No fonts exist.

</td>
</tr>
</table>
 

The following error codes can be returned for the <a href="/windows/desktop/api/commdlg/nf-commdlg-getopenfilenamea">GetOpenFileName</a> and <a href="/windows/desktop/api/commdlg/nf-commdlg-getsavefilenamea">GetSaveFileName</a> functions.

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>FNERR_BUFFERTOOSMALL</b></dt>
<dt>0x3003</dt>
</dl>
</td>
<td width="60%">
The buffer pointed to by the <b>lpstrFile</b> member of the <a href="/windows/win32/api/commdlg/ns-commdlg-openfilenamea">OPENFILENAME</a> structure is too small for the file name specified by the user. The first two bytes of the 
							<b>lpstrFile</b> buffer contain an integer value specifying the size required to receive the full name, in 
							characters.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>FNERR_INVALIDFILENAME</b></dt>
<dt>0x3002</dt>
</dl>
</td>
<td width="60%">
A file name is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>FNERR_SUBCLASSFAILURE</b></dt>
<dt>0x3001</dt>
</dl>
</td>
<td width="60%">
An attempt to subclass a list box failed because sufficient memory was not available.

</td>
</tr>
</table>
 

The following error code can be returned for the <a href="/windows/desktop/api/commdlg/nf-commdlg-findtexta">FindText</a> and <a href="/windows/desktop/api/commdlg/nf-commdlg-replacetexta">ReplaceText</a> functions.

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>FRERR_BUFFERLENGTHZERO</b></dt>
<dt>0x4001</dt>
</dl>
</td>
<td width="60%">
A member of the <a href="/windows/desktop/api/commdlg/ns-commdlg-findreplacea">FINDREPLACE</a> structure points to an invalid buffer.

</td>
</tr>
</table>

## -see-also

<a href="/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1">CHOOSECOLOR</a>



<a href="/windows/desktop/api/commdlg/ns-commdlg-choosefonta">CHOOSEFONT</a>



<a href="/previous-versions/windows/desktop/legacy/ms646912(v=vs.85)">ChooseColor</a>



<a href="/previous-versions/windows/desktop/legacy/ms646914(v=vs.85)">ChooseFont</a>



<a href="/windows/desktop/dlgbox/common-dialog-box-library">Common Dialog Box Library</a>



<b>Conceptual</b>



<a href="/windows/desktop/api/commdlg/ns-commdlg-devnames">DEVNAMES</a>



<a href="/windows/desktop/api/winuser/nf-winuser-dialogboxa">DialogBox</a>



<a href="/windows/desktop/api/commdlg/ns-commdlg-findreplacea">FINDREPLACE</a>



<a href="/windows/desktop/api/commdlg/nf-commdlg-findtexta">FindText</a>



<a href="/windows/desktop/api/commdlg/nf-commdlg-getopenfilenamea">GetOpenFileName</a>



<a href="/windows/desktop/api/commdlg/nf-commdlg-getsavefilenamea">GetSaveFileName</a>



<a href="/windows/win32/api/commdlg/ns-commdlg-openfilenamea">OPENFILENAME</a>



<a href="/windows/win32/api/commdlg/ns-commdlg-pagesetupdlga">PAGESETUPDLG</a>



<a href="/windows/win32/api/commdlg/ns-commdlg-printdlga">PRINTDLG</a>



<a href="/previous-versions/windows/desktop/legacy/ms646937(v=vs.85)">PageSetupDlg</a>



<a href="/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)">PrintDlg</a>



<b>Reference</b>



<a href="/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea">RegisterWindowMessage</a>



<a href="/windows/desktop/api/commdlg/nf-commdlg-replacetexta">ReplaceText</a>
