---
UID: NC:prsht.PFNPROPSHEETCALLBACK
title: PFNPROPSHEETCALLBACK (prsht.h)
description: An application-defined callback function that the system calls when the property sheet is being created and initialized.helpviewer_keywords: ["PFNPROPSHEETCALLBACK","PSCB_BUTTONPRESSED","PSCB_INITIALIZED","PSCB_PRECREATE","PropSheetProc","PropSheetProc callback","PropSheetProc callback function [Windows Controls]","_win32_PropSheetProc","_win32_PropSheetProc_cpp","controls.PropSheetProc","controls._win32_PropSheetProc","prsht/PFNPROPSHEETCALLBACK","prsht/PropSheetProc"]
old-location: controls\PropSheetProc.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\propsheet\functions\propsheetproc.htm
ms.date: 12/05/2018
ms.keywords: PFNPROPSHEETCALLBACK, PSCB_BUTTONPRESSED, PSCB_INITIALIZED, PSCB_PRECREATE, PropSheetProc, PropSheetProc callback, PropSheetProc callback function [Windows Controls], _win32_PropSheetProc, _win32_PropSheetProc_cpp, controls.PropSheetProc, controls._win32_PropSheetProc, prsht/PFNPROPSHEETCALLBACK, prsht/PropSheetProc
f1_keywords:
- prsht/PropSheetProc
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# PFNPROPSHEETCALLBACK callback function


## -description


An application-defined callback function that the system calls when the property sheet is being created and initialized.


## -parameters




### -param Arg1


### -param Arg2


### -param Arg3








#### - hwndDlg

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Handle to the property sheet dialog box.


#### - lParam

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">LPARAM</a></b>

Additional information about the message. The meaning of this value depends on the <i>uMsg</i> parameter. 

If <i>uMsg</i> is  PSCB_INITIALIZED or PSCB_BUTTONPRESSED, the value of <i>lParam</i> is zero.

If <i>uMsg</i> is PSCB_PRECREATE, then <i>lParam</i> will be a pointer to either a  <a href="https://docs.microsoft.com/windows/desktop/api/winuser/ns-winuser-dlgtemplate">DLGTEMPLATE</a> or <a href="https://docs.microsoft.com/windows/desktop/dlgbox/dlgtemplateex">DLGTEMPLATEEX</a> structure describing the property sheet dialog box. Test the signature of the structure to determine the type. If signature is equal to 0xFFFF then the structure is an extended dialog template, otherwise the structure is a standard dialog template.


```

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



#### - uMsg

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Message being received. This parameter is one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="PSCB_BUTTONPRESSED"></a><a id="pscb_buttonpressed"></a><dl>
<dt><b>PSCB_BUTTONPRESSED</b></dt>
</dl>
</td>
<td width="60%">

<a href="https://docs.microsoft.com/windows/desktop/Controls/common-control-versions">Version 6.0</a> and later. Indicates the user pressed a button in the property sheet dialog box. To enable this, specify PSH_USECALLBACK in <a href="https://docs.microsoft.com/windows/desktop/api/prsht/ns-prsht-propsheetheadera_v2">PROPSHEETHEADER.dwFlags</a> and specify the name of this callback function in <b>PROPSHEETHEADER.pfnCallback</b>. The <i>lParam</i> value is one of the following. Note that only PSBTN_CANCEL is valid when you are using the Aero wizard style (<b>PSH_AEROWIZARD</b>).

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
 

Note that Comctl32.dll versions 6 and later are not redistributable. To use these versions of Comctl32.dll, specify the particular version in a manifest. For more information on manifests, see <a href="https://docs.microsoft.com/windows/desktop/Controls/cookbook-overview">Enabling Visual Styles</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="PSCB_INITIALIZED"></a><a id="pscb_initialized"></a><dl>
<dt><b>PSCB_INITIALIZED</b></dt>
</dl>
</td>
<td width="60%">
Indicates that the property sheet is being initialized. The <i>lParam</i> value is zero for this message.

</td>
</tr>
<tr>
<td width="40%"><a id="PSCB_PRECREATE"></a><a id="pscb_precreate"></a><dl>
<dt><b>PSCB_PRECREATE</b></dt>
</dl>
</td>
<td width="60%">
Indicates that the property sheet is about to be created. The <i>hwndDlg</i> parameter is <b>NULL</b>, and the <i>lParam</i> parameter is the address of a dialog template in memory. This template is in the form of a <a href="https://docs.microsoft.com/windows/desktop/api/winuser/ns-winuser-dlgtemplate">DLGTEMPLATE</a> or <a href="https://docs.microsoft.com/windows/desktop/dlgbox/dlgtemplateex">DLGTEMPLATEEX</a> structure followed by one or more <a href="https://docs.microsoft.com/windows/desktop/api/winuser/ns-winuser-dlgitemtemplate">DLGITEMTEMPLATE</a> structures. This message is not applicable if you are using the Aero wizard style (<a href="https://docs.microsoft.com/windows/desktop/api/prsht/ns-prsht-propsheetheadera_v2">PSH_AEROWIZARD</a>).

</td>
</tr>
</table>
 


## -returns



Type: <b>int</b>

Returns zero.




## -remarks



To enable a <i>PropSheetProc</i> callback function, use the <a href="https://docs.microsoft.com/windows/desktop/api/prsht/ns-prsht-propsheetheadera_v2">PROPSHEETHEADER</a> structure when you call the <a href="https://docs.microsoft.com/windows/desktop/api/prsht/nf-prsht-propertysheeta">PropertySheet</a> function to create the property sheet. Use the <b>pfnCallback</b> member to specify an address of the callback function, and set the <b>PSP_USECALLBACK</b> flag in the <b>dwFlags</b> member.

<i>PropSheetProc</i> is a placeholder for the application-defined function name. The <b>PFNPROPSHEETCALLBACK</b> type is the address of a <i>PropSheetProc</i> callback function.



