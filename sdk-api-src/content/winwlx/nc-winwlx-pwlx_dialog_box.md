---
UID: NC:winwlx.PWLX_DIALOG_BOX
title: PWLX_DIALOG_BOX (winwlx.h)
description: Called by the GINA to create a modal dialog box from a dialog box template.
helpviewer_keywords: ["PWLX_DIALOG_BOX","PWLX_DIALOG_BOX callback","WlxDialogBox","WlxDialogBox callback function [Security]","_gina_wlxdialogbox","security.wlxdialogbox","winwlx/WlxDialogBox"]
old-location: security\wlxdialogbox.htm
tech.root: security
ms.assetid: a16313ea-ae76-4d9b-80b3-3fb12af803c7
ms.date: 12/05/2018
ms.keywords: PWLX_DIALOG_BOX, PWLX_DIALOG_BOX callback, WlxDialogBox, WlxDialogBox callback function [Security], _gina_wlxdialogbox, security.wlxdialogbox, winwlx/WlxDialogBox
req.header: winwlx.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
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
 - PWLX_DIALOG_BOX
 - winwlx/PWLX_DIALOG_BOX
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - winwlx.h
api_name:
 - WlxDialogBox
---

# PWLX_DIALOG_BOX callback function


## -description

<p class="CCE_Message">[The WlxDialogBox function is no longer available for use as of Windows Server 2008 and Windows Vista.]

Called by the <a href="/windows/desktop/SecGloss/g-gly">GINA</a> to create a modal dialog box from a dialog box template.
<div class="alert"><b>Note</b>   GINA DLLs are ignored in Windows Vista.</div><div> </div>

## -parameters

### -param hWlx [in]

Specifies the Winlogon handle passed to GINA in the 
<a href="/windows/desktop/api/winwlx/nf-winwlx-wlxinitialize">WlxInitialize</a> call.

### -param hInst [in]

Specifies an instance of the module whose executable file contains the dialog box template.

### -param lpszTemplate [in]

Specifies the dialog box template. This parameter is either the address of a null-terminated character string that specifies the name of the dialog box template, or an integer value that specifies the resource identifier of the dialog box template. If the parameter specifies a resource identifier, its high-order word must be zero and its low-order word must contain the identifier. You can use the 
<a href="/windows/desktop/api/winuser/nf-winuser-makeintresourcea">MAKEINTRESOURCE</a> macro to create this value.

### -param hwndOwner [in]

Specifies the window that owns the dialog box.

### -param dlgprc [in]

Points to the dialog box procedure. For more information about the dialog box procedure, see the 
<a href="/windows/desktop/api/winuser/nc-winuser-dlgproc">DialogProc</a> callback function.

## -returns

If the <b>WlxDialogBox</b> function succeeds, the return value is the <i>nResult</i> parameter given in the call to the 
<a href="/windows/desktop/api/winuser/nf-winuser-enddialog">EndDialog</a> function used to terminate the dialog box. The following table lists some possible success return values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WLX_DLG_INPUT_TIMEOUT</b></dt>
</dl>
</td>
<td width="60%">
Input timed out.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WLX_DLG_SAS</b></dt>
</dl>
</td>
<td width="60%">
A <a href="/windows/desktop/SecGloss/s-gly">secure attention sequence</a> (SAS) event occurred.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WLX_DLG_SCREEN_SAVER_TIMEOUT</b></dt>
</dl>
</td>
<td width="60%">
The screen saver timed out.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WLX_DLG_USER_LOGOFF</b></dt>
</dl>
</td>
<td width="60%">
The user logged off.

</td>
</tr>
</table>
 

If the function fails, the return value is –1.

## -remarks

GINA must use the Winlogon <b>WlxDialogBox</b> function, not the Windows <a href="/windows/desktop/api/winuser/nf-winuser-dialogboxa">DialogBox</a> macro. <b>WlxDialogBox</b> duplicates the Windows <b>DialogBox</b> macro, and also allows Winlogon to terminate the dialog box. For more information, see 
<b>DialogBox</b>.

## -see-also

<a href="/windows/desktop/api/winuser/nf-winuser-dialogboxa">DialogBox</a>



<a href="/windows/desktop/api/winuser/nc-winuser-dlgproc">DialogProc</a>



<a href="/windows/desktop/api/winuser/nf-winuser-enddialog">EndDialog</a>



<a href="/windows/desktop/api/winuser/nf-winuser-makeintresourcea">MAKEINTRESOURCE</a>



<a href="/windows/desktop/api/winwlx/nf-winwlx-wlxinitialize">WlxInitialize</a>