---
UID: NC:prsht.PFNPROPSHEETCALLBACK
title: PFNPROPSHEETCALLBACK (prsht.h)
description: An application-defined callback function that the system calls when the property sheet is being created and initialized.
helpviewer_keywords: ["PFNPROPSHEETCALLBACK","PSCB_BUTTONPRESSED","PSCB_INITIALIZED","PSCB_PRECREATE","PropSheetProc","PropSheetProc callback","PropSheetProc callback function [Windows Controls]","_win32_PropSheetProc","_win32_PropSheetProc_cpp","controls.PropSheetProc","controls._win32_PropSheetProc","prsht/PFNPROPSHEETCALLBACK","prsht/PropSheetProc"]
old-location: controls\PropSheetProc.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\propsheet\functions\propsheetproc.htm
ms.date: 12/05/2018
ms.keywords: PFNPROPSHEETCALLBACK, PSCB_BUTTONPRESSED, PSCB_INITIALIZED, PSCB_PRECREATE, PropSheetProc, PropSheetProc callback, PropSheetProc callback function [Windows Controls], _win32_PropSheetProc, _win32_PropSheetProc_cpp, controls.PropSheetProc, controls._win32_PropSheetProc, prsht/PFNPROPSHEETCALLBACK, prsht/PropSheetProc
req.header: prsht.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - PFNPROPSHEETCALLBACK
 - prsht/PFNPROPSHEETCALLBACK
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Prsht.h
api_name:
 - PropSheetProc
 - PFNPROPSHEETCALLBACK
---

# PFNPROPSHEETCALLBACK callback function


## -description

An application-defined callback function that the system calls when the property sheet is being created and initialized.

## -parameters

### -param unnamedParam1

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Handle to the property sheet. This parameter is typically called *hWnd*.

### -param unnamedParam2

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Message being received. This parameter is typically called *uMsg*.

This parameter is one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>

<tr>
<td width="40%"><a id="PSCB_INITIALIZED"></a><a id="pscb_initialized"></a><dl>
<dt><b>PSCB_INITIALIZED (1)</b></dt>
</dl>
</td>
<td width="60%">
Indicates that the property sheet is being initialized. The <i>lParam</i> (<i>unnamedParam3</i>) value is zero for this message.

</td>
</tr>
<tr>
<td width="40%"><a id="PSCB_PRECREATE"></a><a id="pscb_precreate"></a><dl>
<dt><b>PSCB_PRECREATE (2)</b></dt>
</dl>
</td>
<td width="60%">
Indicates that the property sheet is about to be created. The <i>hWnd</i> (<i>unnamedParam1</i>) parameter is <b>NULL</b>, and the <i>lParam</i> (<i>unnamedParam3</i>) parameter is the address of a dialog template in memory. This template is in the form of a <a href="../winuser/ns-winuser-dlgtemplate.md">DLGTEMPLATE</a> or <a href="/windows/win32/dlgbox/dlgtemplateex">DLGTEMPLATEEX</a> structure followed by one or more <a href="../winuser/ns-winuser-dlgitemtemplate.md">DLGITEMTEMPLATE</a> structures. This message is not applicable if you are using the Aero wizard style (<a href="/windows/win32/controls/pss-propsheetheader">PSH_AEROWIZARD</a>).

</td>
</tr>

<tr>
<td width="40%"><a id="PSCB_BUTTONPRESSED"></a><a id="pscb_buttonpressed"></a><dl>
<dt><b>PSCB_BUTTONPRESSED (3)</b></dt>
</dl>
</td>
<td width="60%">

<a href="/windows/win32/Controls/common-control-versions">Version 6.0</a> and later. Indicates the user pressed a button in the property sheet dialog box. To enable this, specify PSH_USECALLBACK in <a href="/windows/win32/controls/pss-propsheetheader">PROPSHEETHEADER.dwFlags</a> and specify the name of this callback function in <b>PROPSHEETHEADER.pfnCallback</b>. The <i>lParam</i> (<i>Arg3</i>) value is one of the following. Note that only PSBTN_CANCEL is valid when you are using the Aero wizard style (<b>PSH_AEROWIZARD</b>).

<table class="clsStd">
<tr>
<th>Button pressed</th>
<th>lParam value</th>
</tr>
<tr>
<td>OK</td>
<td>PSBTN_OK</td>
</tr>
<tr>
<td>Cancel</td>
<td>PSBTN_CANCEL</td>
</tr>
<tr>
<td>Apply</td>
<td>PSBTN_APPLYNOW</td>
</tr>
<tr>
<td>Close</td>
<td>PSBTN_FINISH</td>
</tr>
</table>

Note that Comctl32.dll versions 6 and later are not redistributable. To use these versions of Comctl32.dll, specify the particular version in a manifest. For more information on manifests, see <a href="/windows/win32/controls/cookbook-overview">Enabling Visual Styles</a>.

</td>
</tr>

</table>

### -param unnamedParam3

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPARAM</a></b>

Additional information about the message. This parameter is typically called *lParam*.

The meaning of this value depends on the *uMsg* (*unnamedParam2*) parameter:

* If *uMsg* is  PSCB_INITIALIZED or PSCB_BUTTONPRESSED, the value of this parameter is zero.
* If *uMsg* is PSCB_PRECREATE, then this parameter will be a pointer to either a  <a href="../winuser/ns-winuser-dlgtemplate.md">DLGTEMPLATE</a> or <a href="/windows/win32/dlgbox/dlgtemplateex">DLGTEMPLATEEX</a> structure describing the property sheet dialog box. Test the signature of the structure to determine the type. If signature is equal to 0xFFFF then the structure is an extended dialog template, otherwise the structure is a standard dialog template. The following example demonstrates how to do this.

    ```cpp
    if (uMsg == PSCB_PRECREATE) 
    {
         if (lParam)
         {
              DLGTEMPLATE *pDlgTemplate;
              DLGTEMPLATEEX *pDlgTemplateEx;
              
              pDlgTemplateEx = (DLGTEMPLATEEX *)lParam;  
              if (pDlgTemplateEx->signature == 0xFFFF)
              {
                   // pDlgTemplateEx points to an extended  
                   // dialog template structure.
              }
              else
              {
                   // This is a standard dialog template
                   //  structure.
                   pDlgTemplate = (DLGTEMPLATE *)lParam;
              }
         }    
    }
    ```

## -returns

Type: <b>int</b>

Returns zero.

## -remarks

To enable a *PropSheetProc* callback function, use the <a href="/windows/win32/controls/pss-propsheetheader">PROPSHEETHEADER</a> structure when you call the <a href="/windows/desktop/api/prsht/nf-prsht-propertysheeta">PropertySheet</a> function to create the property sheet. Use the *pfnCallback* member to specify an address of the callback function, and set the PSP_USECALLBACK flag in the *dwFlags* member.

*PropSheetProc* is a placeholder for the application-defined function name. The **PFNPROPSHEETCALLBACK** type is the address of a *PropSheetProc* callback function.
